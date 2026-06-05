# Lock-In Supply Overhang

## Default Lock-In Tranches

Read the offer document. Use these defaults only when the disclosed terms do not override them.

| Tranche | Default lock-in | Note |
|---|---:|---|
| Anchor investors, first 50% | 30 days from allotment | First anchor supply test |
| Anchor investors, remaining 50% | 90 days from allotment | Second anchor supply test |
| Non-promoter pre-issue capital | 6 months from allotment | Subject to exemptions and special cases |
| Promoter holding above minimum promoter contribution | 6 months from allotment | Excess promoter holding |
| Minimum promoter contribution | 18 months from allotment | Longer period can apply in specified capex-heavy fresh issue cases |
| Pledged/frozen pre-IPO shares | Applicable lock-in or non-transferable marking | Check 2026 non-transferability disclosures |

Use allotment date for lock-in clocks unless the offer document says otherwise. Display absolute dates.

```text
Anchor 30-day unlock = allotment date + 30 days
Anchor 90-day unlock = allotment date + 90 days
Pre-IPO/non-promoter unlock = allotment date + 6 months
Promoter excess unlock = allotment date + 6 months
Minimum promoter contribution unlock = allotment date + 18 months
```

## Share Extraction

Extract from the offer document:

- Total pre-issue and post-issue share capital.
- Promoter shares, minimum promoter contribution, and excess promoter shares.
- Non-promoter pre-issue shares.
- Pre-IPO investor names, shares, acquisition dates, and cost where disclosed.
- Anchor allocation shares and investor names.
- ESOP, employee trust, convertible, CCPS, CCD, warrants, and other dilution.
- Exempt or specially locked shares.

## Sell Probability Heuristics

| Holder type | Sell probability | Reason |
|---|---:|---|
| Domestic mutual fund anchor | 25-50% | May hold quality IPOs but can rebalance |
| FPI anchor | 40-70% | More market/flow sensitive |
| Insurance/pension/long-only anchor | 15-40% | Longer holding horizon |
| Hedge fund/HNI-style anchor | 50-80% | Higher turnover |
| PE/VC pre-IPO fund | 60-90% | Fund lifecycle and large gains |
| Strategic investor | 15-40% | Business relationship may matter |
| Promoter excess | 10-35% | Control and signal concerns reduce selling |
| Minimum promoter contribution | 5-15% | Lower probability but high headline risk |
| ESOP/employee trust | 20-60% | Wealth realization varies by vesting and price |

If acquisition cost is disclosed:

```text
Unrealized gain at current price = current price / acquisition cost - 1
```

High gains increase sell incentive. Label cost-basis inference clearly when exact acquisition cost is unavailable.

## Overhang Metrics

```text
Expected sellable shares = unlock shares * holder sell probability
Overhang ratio = expected sellable shares / 60-trading-day average daily traded volume
```

| Overhang ratio | Score | Expected behavior |
|---:|---|---|
| <20 trading days | Low | Usually absorbable unless sentiment is weak |
| 20-60 trading days | Moderate | Price may weaken before event |
| 60-120 trading days | High | Selling can dominate near event |
| >120 trading days | Extreme | Major thesis risk |

Also show unlock percent of free float, unlock percent of total shares, expected sell value, and expected sell value / 60-day average daily traded value.

## Event Windows

Analyze pressure around:

- T-10 to T-1 trading days before unlock: anticipation and positioning.
- T day to T+5 trading days: actual unlock and block/bulk deal risk.
- Unlock day +6 to unlock day +20 trading days: absorption or continued drift.

If a block deal happens before unlock, reduce day-of pressure but keep the supply note.
