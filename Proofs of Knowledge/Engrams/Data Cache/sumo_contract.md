To execute the purpose of designing a smart contract that best distributes seigniorage based on onchain sumo bets, the entire process can be broken down into the following steps:

1. **Betting Stakes and Inflation**: Users bet on sumo matches via smart contract by staking tokens. This can be done by sending a specified amount of tokens to the smart contract along with an identifier for the wrestler they're betting on. The total amount of tokens staked influences the inflation rate of the currency, creating more tokens.

```solidity
function stakeBet(uint256 amount, uint256 wrestlerId) public {
    require(token.transferFrom(msg.sender, address(this), amount));
    // Record the bet in the contract state
    bets[msg.sender][wrestlerId] = amount;
}
```

2. **Calculating Match Outcome and Token Distribution**: After a match, the contract uses the binary outcome to distribute the newly created (inflated) tokens. Winners get a proportionally higher share of the new tokens, and losers also get a smaller share of the new tokens to ensure that nobody loses.

```solidity
function distributeWinnings(uint256 winningWrestlerId) public {
    uint256 totalStaked = getTotalStaked();
    uint256 inflation = calculateInflation(totalStaked); 

    // Distribute a proportion of inflated tokens based on staked amount
    for (address bettor : bettors) {
        if (bets[bettor][winningWrestlerId] > 0) {
            uint256 winnings = calculateWinnings(bettor, winningWrestlerId, inflation);
            token.transfer(bettor, winnings);
        }
        else {
            uint256 consolation = calculateConsolation(bettor, winningWrestlerId, inflation);
            token.transfer(bettor, consolation);
        }
    }
}
```

3. **Seigniorage Profits**: In this system, nobody has to lose tokens if their bet was wrong. The seigniorage profit comes from the inflation mechanism and the increase in each user's token holding.

Please note that the code snippets are pseudo-code and don't cover necessary contract details like security, initialization, and other features. You'd need a professional solidity developer to design and audit the final contract, and potentially deploy several versions on a testnet. 

This mechanism encourages users to participate in the system with a win-win scenario as every participant gets a portion of the newly minted tokens depending on their wager. However, it's essential to carefully manage token inflation as excessive inflation can lead to devaluation of the tokens.