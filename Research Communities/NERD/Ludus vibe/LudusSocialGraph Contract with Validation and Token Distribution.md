The system comprised of LudusSocialGraph, validation, and token mechanisms need to be interconnected in a holistic manner. Here's how:

## LudusSocialGraph Contract with Validation and Token Distribution

```solidity
pragma solidity ^0.8.21;

import "./LudusToken.sol";
import "@openzeppelin/contracts/token/ERC721/IERC721.sol";

contract LudusSocialGraph {

    struct MatchResult {
        string matchDetails;
        bool isScoreValidated;
    }

    struct Athlete {
        string name;
        string profileUrl;
        uint tokenId; // ERC721 token ID representing athlete profile
        MatchResult[] matchResults;
    }

    mapping(address => Athlete) public athletes;
    mapping(uint => MatchResult) public pendingMatchResults;
    LudusToken public ludusToken;
    IERC721 public athleteProfileToken; // Athlete profile ERC721 token contract
  
    constructor(address _ludusTokenAddress, address _athleteProfileTokenAddress) {
        ludusToken = LudusToken(_ludusTokenAddress);
        athleteProfileToken = IERC721(_athleteProfileTokenAddress);
    }

    function registerAthlete(string memory _name, string memory _profileUrl, uint256 _tokenId) public {
        require(bytes(_name).length > 0, "Name is required");

        Athlete storage athlete = athletes[msg.sender];
        require(bytes(athlete.name).length == 0, "Athlete already registered");

        athlete.name = _name;
        athlete.profileUrl = _profileUrl;
        athlete.tokenId = _tokenId;

        athleteProfileToken.transferFrom(msg.sender, address(this), _tokenId); // Transfer the athlete profile NFT to the contract

        ludusToken.mint(msg.sender, 100); // Minting 100 Ludus tokens for new athlete
    }
    
    function publishMatchResult(string memory _matchDetails) public {
        Athlete storage athlete = athletes[msg.sender];
        require(bytes(athlete.name).length > 0, "Athlete not found");

        MatchResult memory newMatch = MatchResult(_matchDetails, false);
        athlete.matchResults.push(newMatch);

        uint matchId = athlete.matchResults.length - 1;
        pendingMatchResults[matchId] = newMatch;
    }

    function validateMatchResult(uint _matchId) public {
        require(pendingMatchResults[_matchId].isScoreValidated == true, "Match result not yet validated");
        delete pendingMatchResults[_matchId];
        ludusToken.mint(msg.sender, 100);  // The validated match result triggers minting of 100 new Ludus tokens
    }
}
```

In this contract:
- We've added a structure for `MatchResult`, which includes match details and a validation status.
- `Athlete` struct now includes an array for storing `MatchResult`.
- A new function, `publishMatchResult`, is added to allow athletes to submit match results, which are stored as pending validation.
- `validateMatchResult` function checks if a match is validated and, once validated, it mints additional tokens for the athlete. 

This contract unifies the LudusSocialGraph, match result validation, and Ludus token distribution. The system encourages participation and accurately rewards the involved parties based on their involvement, while also ensuring match results are valid and fair.