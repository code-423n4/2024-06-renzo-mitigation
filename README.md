# Renzo Mitigation Review
- Total Prize Pool: $32,500 in USDC
  - HM awards: $29,000 in USDC
  - Judge awards: $3,500 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2024-06-renzo-mitigation-review/submit)
- Starts June 3, 2024 20:00 UTC 
- Ends June 7, 2024 20:00 UTC 

## Important note 

Each warden must submit a mitigation review for *every* individual PR listed in the `Scope` section below. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and listed here.

### High Findings

- [H-01: Withdrawals can be locked forever if recipient is a contract](https://github.com/code-423n4/2024-04-renzo-findings/issues/612)
- [H-02: Incorrect calculation of queued withdrawals can deflate TVL and increase ezETH mint rate](https://github.com/code-423n4/2024-04-renzo-findings/issues/395)
- [H-03: ETH withdrawals from EigenLayer always fail due to OperatorDelegator's nonReentrant receive()](https://github.com/code-423n4/2024-04-renzo-findings/issues/368)
- [H-04: Withdrawals logic allows MEV exploits of TVL changes and zero-slippage zero-fee swaps](https://github.com/code-423n4/2024-04-renzo-findings/issues/326)
- [H-05: Withdrawals of rebasing tokens can lead to insolvency and unfair distribution of protocol reserves](https://github.com/code-423n4/2024-04-renzo-findings/issues/282)
- [H-06: The amount of xezETH in circulation will not represent the amount of ezETH tokens 1:1](https://github.com/code-423n4/2024-04-renzo-findings/issues/145)
- [H-07: DOS of completeQueuedWithdrawal when ERC20 buffer is filled](https://github.com/code-423n4/2024-04-renzo-findings/issues/87)
- [H-08: Incorrect withdraw queue balance in TVL calculation](https://github.com/code-423n4/2024-04-renzo-findings/issues/28)

### Medium Findings
- [M-01: Withdrawals can fail due to deposits reverting in completeQueuedWithdrawal()](https://github.com/code-423n4/2024-04-renzo-findings/issues/604)
- [M-02: Withdrawals and Claims are meant to be pausable, but it is not possible in practice](https://github.com/code-423n4/2024-04-renzo-findings/issues/569)
- [M-03: Fixed hearbeat used for price validation is too stale for some tokens](https://github.com/code-423n4/2024-04-renzo-findings/issues/563)
- [M-04: Price updating mechanism can break](https://github.com/code-423n4/2024-04-renzo-findings/issues/519)
- [M-05: calculateTVL may run out of gas for modest number of operators and tokens breaking deposits, withdrawals, and trades](https://github.com/code-423n4/2024-04-renzo-findings/issues/514)
- [M-06: L1::xRenzoBridge and L2::xRenzoBridge uses the block.timestamp as dependency, which can cause issue.](https://github.com/code-423n4/2024-04-renzo-findings/issues/502)
- [M-07: Lack of slippage and deadline during withdraw and deposit](https://github.com/code-423n4/2024-04-renzo-findings/issues/484)
- [M-08: Not handling the failure of cross chain messaging](https://github.com/code-423n4/2024-04-renzo-findings/issues/373)
- [M-09: Deposits will always revert if the amount being deposited is less than the bufferToFill value](https://github.com/code-423n4/2024-04-renzo-findings/issues/198)
- [M-10: Potential Arbitrage Opportunity in the xRenzoDeposit L2 contract](https://github.com/code-423n4/2024-04-renzo-findings/issues/135)
- [M-11: Fetched price from the oracle is not stored in xRenzoDeposit](https://github.com/code-423n4/2024-04-renzo-findings/issues/117)
- [M-12: Incorrect exchange rate provided to Balancer pools](https://github.com/code-423n4/2024-04-renzo-findings/issues/113)
- [M-13: Pending withdrawals prevent safe removal of collateral assets](https://github.com/code-423n4/2024-04-renzo-findings/issues/103)
- [M-14: stETH/ETH Feed being used opens up to 2 way deposit<->withdrawal arbitrage](https://github.com/code-423n4/2024-04-renzo-findings/issues/13)

[ ⭐️ SPONSORS ADD INFO HERE ]

## Overview of changes

Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern.

## Scope

### Branch
[ ⭐️ SPONSORS ADD A LINK TO THE BRANCH IN YOUR REPO CONTAINING ALL PRS ]

### Mitigation of High & Medium Severity Issues
[ ⭐️ SPONSORS ADD ALL RELEVANT PRs TO THE TABLE BELOW:]

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/your-repo/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

### Additional scope to be reviewed
[ ⭐️ CAS PLEASE REMOVE THIS SECTION IF THE SPONSOR IS ONLY MITIGATING HMS]

[ ⭐️ SPONSORS ADD ALL RELEVANT PRs TO THE TABLE BELOW:]

These are additional changes that will be in scope.

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/your-repo/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
