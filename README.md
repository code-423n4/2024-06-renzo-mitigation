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
- [H-07: DOS of completeQueuedWithdrawal when ERC20 buffer is filled](https://github.com/code-423n4/2024-04-renzo-findings/issues/87)
- [H-08: Incorrect withdraw queue balance in TVL calculation](https://github.com/code-423n4/2024-04-renzo-findings/issues/28)

### Medium Findings
- [M-02: Withdrawals and Claims are meant to be pausable, but it is not possible in practice](https://github.com/code-423n4/2024-04-renzo-findings/issues/569)
- [M-09: Deposits will always revert if the amount being deposited is less than the bufferToFill value](https://github.com/code-423n4/2024-04-renzo-findings/issues/198)
- [M-12: Incorrect exchange rate provided to Balancer pools](https://github.com/code-423n4/2024-04-renzo-findings/issues/113)



## Scope

### Branch

https://github.com/Renzo-Protocol/Contracts

### Mitigation of High & Medium Severity Issues

| URL                                                                                                                                                                        | Mitigation of |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| https://github.com/Renzo-Protocol/Contracts/pull/109                                                                                                                       | H-01          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/89a344ba837d98018b63a450666a72b0827aa8cf                                                                       | H-02          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/5700b8dd6318b6ac1c7a50875a12b167da65f032                                                                       | H-03          |
| https://github.com/Renzo-Protocol/Contracts/pull/111                                                                                                                       | H-04          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/647bc4ca9fa181bf87f1b885e09a887bd0eb6c7c                                                                       | H-07          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/2e4f4c6701ed004c2f10addde2d3089ac1b3d032                                                                       | H-08          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/2e4f4c6701ed004c2f10addde2d3089ac1b3d032                                                                       | M-02          |
| https://github.com/Renzo-Protocol/Contracts/pull/87/commits/89a344ba837d98018b63a450666a72b0827aa8cf#diff-9ef0de77fd5c84001c61efd21485131caa42626118759d9ae76d8b652726dc8c | M-09          |
| https://github.com/Renzo-Protocol/Contracts/pull/113                                                                                                                       | M-12          |

## Out of Scope

Any findings that were acknowledged, disputed or in QA reports from the past audit.

- H-05: Withdrawals of rebasing tokens can lead to insolvency and unfair distribution of protocol reserves
- H-06: The amount of xezETH in circulation will not represent the amount of ezETH tokens 1:1
- M-01: Withdrawals can fail due to deposits reverting in completeQueuedWithdrawal()
- M-03: Fixed hearbeat used for price validation is too stale for some tokens
- M-04: Price updating mechanism can break
- M-05: calculateTVL may run out of gas for modest number of operators and tokens breaking deposits, withdrawals, and trades
- M-06: L1::xRenzoBridge and L2::xRenzoBridge uses the block.timestamp as dependency, which can cause issue.
- M-07: Lack of slippage and deadline during withdraw and deposit
- M-08: Not handling the failure of cross chain messaging
- M-10: Potential Arbitrage Opportunity in the xRenzoDeposit L2 contract
- M-11: Fetched price from the oracle is not stored in xRenzoDeposit
- M-13: Pending withdrawals prevent safe removal of collateral assets
- M-14: stETH/ETH Feed being used opens up to 2 way deposit<->withdrawal arbitrage
