
# MIP40c3-SPXX: Modify Core Unit Budget (MKR) - Maker Talent (MT-001).

## Preamble

```
MIP40c3-SP#: XX
Author(s): @manomad_
Contributors: @synesthesia
Tags: core-unit, budget, dai-budget, makertalent, mkr incentives
Status: Request For Comments (RFC)
Date Applied: <2021-12-08>
Date Ratified: <yyyy-mm-dd>
```

## Sentence Summary

MIP40c3-SPXX adds the MKR Incentive Plan budget for Core Unit MT-001: Maker Talent.

## Paragraph Summary

MIP40c3-SPXX adds the MKR Incentive Plan budget for Core Unit MT-001: Maker Talent. It contains:
- Total MKR Expenditure Cap
- Estimated MKR Expenditure (based on the current and projected team)
- Escrow Wallet mechanism

MKR incentives have been determined based on the [Program discussed here](https://forum.makerdao.com/t/pre-mip-discussion-an-alternative-mkr-compensation-plan/8000). This is a 3-year vesting plan with 1-year cliff vest.

## Total MKR Expenditure Cap

The total Expenditure Cap will be `282.41 MKR`.

## Estimated MKR Expenditure

The Estimated MKR Expenditure is our best guess as to how much MKR will be used with the current and forecasted team configuration. The calculation of the MKR Incentives was done taking into account the team at its full projected capacity.

Reasons why the Actual MKR Expenditure could rise closer to the MKR Expenditure Cap:

- A raise for a member of the team;
- New hires;
- Repricing (and resetting) the program, in the event of a bear market.

`Price floor: -30%`. If any Contributor chose to reprice their program, they could do it at a maximum of -30% from the set MKR price.

### Permanent Team Forecast

For the permanent team, this would result in the vesting schedule below.

| Vesting Date  |  MKR Amount  |
|---------------|:------------:|
| MAR, 2022     |        0 MKR |
| SEP, 2022     |    32.08 MKR |
| MAR, 2023     |    35.85 MKR |
| SEP, 2023     |    25.95 MKR |
| MAR, 2024     |    25.95 MKR |
| SEP, 2024     |    25.95 MKR |
| **Total**     |**145.78 MKR**|

This covers the total vesting schedule of `3 years` for the current and forecasted `4 FTEs`.

On average, this yields `12.97 MKR` per FTE per year.

Any changes to these amounts will be reported and reviewed by our budget auditors.

### Parameters

|    Parameter      | Value |
|---------------|:-----:|
| MKR/DAI lock-in Price (New) |   Trailing 6 month average   |
| MKR/DAI lock-in Price |   MKR = $3121.70 (1/SEP/21 - 05/MAR/21)  |
| MKR Price Floor |   -30% ($2185.19)  |
| Vesting Period |   3 years  |
| Cliff Vest |  12 months  |
| Vesting Schedule |   After cliff has expired, biannual MKR amount  |
| Vesting Interval | 6 months  |
| Manual Repricing | yes |
| Auto-Renewal | yes  |

### Payment Implementation

This payment implementation is based on the [SES MKR budget proposal](LINK TO BE ADDED)

- Payment of the MKR tokens will follow the same flow as described in MIP 40 [MT MIP](LINK TO BE ADDED HERE)
- As defined above and in the Monthly Budget Statement it contains the MKR vesting schedule. This schedule specifies when in the future MKR is vesting, and how much.
- To keep the risk acceptable for Maker governance as well as for the team, the MKR is moved from the protocol to the contributors in stages:
  - Following the MKR vesting schedule, any MKR that is vesting in 6 months or less will be included in the top-up transaction which is added to the executive vote. This will move the MKR from the protocol to the `MT Auditors Wallet`, which then acts as an escrow wallet.
  - Following the MKR vesting schedule, after review and approval by the auditors, any MKR that is vesting in 3 months or less will be included in the monthly top-up transaction that moves funds from the `MT Auditors Wallet` to the `MT Permanent Team Operational Wallet`.
  - When the MKR has vested, it is paid out to the contributor, either directly or through an intermediate payment processor.
- Any excess MKR in the `MT Auditors Wallet` or the `MT Permanent Team Operational Wallet` will be returned to the protocol, following the monthly payment transactions.

This payment implementation makes no assumptions about the origin of the MKR. It can either be moved from the protocol’s treasury, newly minted, or obtained from another source.

The MKR that’s held by the `MT Auditors Wallet` and the `MT Permanent Team Operational Wallet` will not be used for voting, signaling, or any other type of governance participation. It will remain in the wallets untouched until it moves to the next step in the process.

MT-001 may consider alternative payment flows compliant with [DssVest](https://forum.makerdao.com/t/mip-54-dssvest/8025) if the standarised flow is compatible with the vesting schedule and that the risk is deemed acceptable by the team.
