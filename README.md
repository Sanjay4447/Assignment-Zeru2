1) Data Collection Method:

The Compound V2 API was not working, so I used randomly generated data to simulate each wallet’s DeFi activity, such as how much they borrowed, supplied, repaid, and how often they were liquidated.

3) Feature Selection:

I used the following features to for wallet’s risk:

- sup: Total supplied amount

- bor: Total borrowed amount

- ratio: Borrow/Supply ratio

- liq: Number of liquidations

- repay: Repayment ratio

3)  Scoring Method:
   
I normalized all the values between 0 and 1 and then calculated the score out of 1000 using this formula:

- score = (0.4 * ratio) + (0.3 * liq) + (0.2 * (1 - repay)) + (0.1 * bor)
- The higher the score, the riskier the wallet

4) Justification of Risk Indicators Used:

- A higher ratio means more borrowing, which is risky

- More liq (liquidations) means poor history

- Low repay means the user didn’t repay properly

- High bor shows more exposure to risk
