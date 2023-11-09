To implement this task, some state variables and constants need to be added to the contract and we can just add constructor arguments to set them, as well as additional functions to update them if appropriate.

We'll need:

1. Storage for the bets made by each address for each wrestler.
2. A list of all bettors to iterate over when distributing tokens.
3. A way to track the total amount staked so that we can adjust the inflation rate accordingly.
4. Calculation for winnings and consolation tokens.

Here's a skeleton of how the contract might look like:

```solidity
//SPDX-License-Identifier: MIT
pragma solidity >=0.8.0 <0.9.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Umo is ERC20 {
    // State variables
    mapping(address => mapping(uint256 => uint256)) public bets;
    address[] public bettors;
    uint256 public totalStaked;

    // Constants
    uint256 public constant WINNING_RATIO = 60; 
    uint256 public constant LOSING_RATIO = 40;

    constructor() ERC20("Umo", "UMO") {
        _mint(msg.sender, 1000000000000000000000000000);
    }
    
    function stakeBet(uint256 amount, uint256 wrestlerId) public {
        _transfer(msg.sender, address(this), amount);
        // Record the bet in the contract state
        bets[msg.sender][wrestlerId] = amount;
        bettors.push(msg.sender);
        totalStaked += amount;
    }

    function distributeWinnings(uint256 winningWrestlerId) public {
        // Calculate inflation
        uint256 inflation = totalStaked * 10 / 100; 
        _mint(address(this), inflation);

        // Distribute inflated tokens based on staked amount
        for (uint i=0; i<bettors.length; i++) {
            address bettor = bettors[i];
            uint256 betAmount = bets[bettor][winningWrestlerId];
            if (betAmount > 0) {
                uint256 winnings = betAmount * inflation * WINNING_RATIO / 100;
                _transfer(address(this), bettor, winnings);
            }
            else {
                uint256 consolation = betAmount * inflation * LOSING_RATIO / 100;
                _transfer(address(this), bettor, consolation);
            }
        }
    }
}
```

In this example, I assumed a simple inflation function where 10% of total stakes gets minted and distributed. The stakers who bet on the winning wrestler receive 60% of the minted tokens proportionally to their stake, and those that bet on the losing wrestler receive the remaining 40%. These ratios can be adjusted as needed.

Please note, the above pseudo-code is a simplified example and doesn't cover necessary contract details like security, best practices and edge cases. Always consider having the final contract reviewed and audited by a Solidity expert before mainnet deployment.