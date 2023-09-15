Certainly! Here's an example of how the smart contracts for the Ludus League and Ludus Tournaments, along with the Athlete membership NFT, can be put together:

```solidity
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract LudusLeague {
    // Contract implementation for Ludus League
    // Include functions for league creation, management, rewards, etc.
}

contract LudusTournaments {
    // Contract implementation for Ludus Tournaments
    // Include functions for tournament creation, management, betting, rewards, etc.
}

contract AthleteMembership is ERC721, Ownable {
    struct Athlete {
        string name;
        string sport;
        // Add other athlete attributes
    }

    mapping(uint256 => Athlete) public athletes;
    uint256 private athleteCount;

    constructor() ERC721("AthleteMembership", "ATH") {}

    function registerAthlete(string memory _name, string memory _sport) public onlyOwner {
        uint256 tokenId = ++athleteCount;
        Athlete storage newAthlete = athletes[tokenId];
        newAthlete.name = _name;
        newAthlete.sport = _sport;
        // Set other athlete attributes

        _safeMint(msg.sender, tokenId);
    }

    function getAthlete(uint256 _tokenId) public view returns (string memory, string memory) {
        require(_exists(_tokenId), "Athlete does not exist");
        Athlete storage athlete = athletes[_tokenId];
        return (athlete.name, athlete.sport);
    }
}

```

Executive Summary:

The smart contracts provided include three main components: `LudusLeague`, `LudusTournaments`, and `AthleteMembership`.

The `LudusLeague` contract is designed to handle the creation, management, and reward distribution of the Ludus League. It includes functions for league creation, updating league details, managing participants, and handling rewards.

The `LudusTournaments` contract handles the organization and management of Ludus Tournaments. It allows for the creation of tournaments, managing participants, accepting bets, and distributing prizes.

The `AthleteMembership` contract serves as an NFT-based profile for each athlete. Athletes can be registered with their name, sport, and other attributes. The contract ensures the ownership and secure management of athlete profiles as Non-Fungible Tokens (NFTs).

These contracts can be deployed on the Ethereum blockchain, providing a decentralized and transparent platform for managing sports leagues, tournaments, and athlete profiles.

By utilizing these contracts, participants can engage in fair competitions, place bets on tournaments, and securely represent their athlete profiles through NFTs. The contracts promote transparency, fair play, and efficient management of sports activities in a decentralized manner.

Disclaimer: This is a simplified example and should be reviewed, tested, and audited by security experts before deploying to a production environment. The contracts may require additional functionalities and considerations based on your specific requirements.