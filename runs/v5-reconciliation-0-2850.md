**Active correction: v5 only, paid epochs 0–2850.**

Use [v5-reconciliation-0-2850.safe.json](./v5-reconciliation-0-2850.safe.json): **14640.560224171410382475 AZTEC to 140 recipients**. It is unsigned and unsent. It replaces the earlier combined v4/v5 correction; do not execute both.

This scope is the nine published v5 batches beginning at epoch 0 and ending at epoch 2850. All were already paid. The correction subtracts each original executed payment and contains only the remainder. All v4 rewards, overpayment offsets and pre-v5 payments are outside this calculation. V5 epoch 2851 onward remains for your next normal run.

The shortfall is **not just fees**:

| Component, after 25% commission | Additional AZTEC owed |
|---|---:|
| 54 omitted earned checkpoints × 262.5 | **14,175** |
| Omitted net sequencer fee rewards | **465.560224171410382475** |
| **Total v5-only correction** | **14,640.560224171410382475** |

A fee-only correction would leave the 54 earned checkpoints unpaid. For example, epochs 2602–2850 paid for 1,169 checkpoints, while 1,182 checkpoints actually earned rewards for this wallet. Those 13 missing checkpoints account for 3,412.5 AZTEC before adding that batch’s fee correction. The separate epoch-1802 boundary omission is included below.

| Paid v5 epochs | Checkpoints paid | Checkpoints earned | Missing | Missing fixed rewards, AZTEC | Fee correction, AZTEC | Total correction, AZTEC |
|---|---:|---:|---:|---:|---:|---:|
| 0–793 | 1253 | 1263 | 10 | 2625 | 4.256485700611832805 | 2629.256485700611832805 |
| 794–1012 | 1146 | 1148 | 2 | 525 | 33.157218596552685041 | 558.157218596552685041 |
| 1013–1277 | 1311 | 1311 | 0 | 0 | 28.359847257762780081 | 28.359847257762780081 |
| 1278–1541 | 1269 | 1274 | 5 | 1312.5 | 280.845947134359866075 | 1593.345947134359866075 |
| 1542–1802 | 1323 | 1326 | 3 | 787.5 | 102.900228530157950965 | 890.400228530157950965 |
| 1803–2071 | 1455 | 1469 | 14 | 3675 | 7.026406082206418138 | 3682.026406082206418138 |
| 2072–2335 | 1228 | 1235 | 7 | 1837.5 | 5.574292912362990483 | 1843.074292912362990483 |
| 2336–2601 | 1277 | 1277 | 0 | 0 | 2.220468362336999749 | 2.220468362336999749 |
| 2602–2850 | 1169 | 1182 | 13 | 3412.5 | 1.219329595058859138 | 3413.719329595058859138 |

The fee column is the delegators’ share, after protocol burn, prover payment, operator commission and per-recipient rounding. Fees are attributed to the recipients whose checkpoints earned them. No fee pool is spread by proposal count.

The amounts above use the same underlying v5 evidence as the earlier full-history audit. The earlier combined total also incorporated v4 corrections and credits; those items are now excluded at your request. The nine v5 batch calculations themselves have not changed.

The [published v5 audit files](https://github.com/NethermindEth/aztec-staking-payout-audit/tree/main/runs) were fetched again and matched to the copies used for verification. All nine reconstructed reward totals match the rollup’s reward-counter changes plus verified claims. The scan contains 11,485 wallet-earned checkpoints. Beneficiaries are verified against the immutable delegation splits at proposal time. No wrong-address payment was found in these nine original batches.

At Ethereum block **26026762**, no new outgoing payments had appeared since the initial reconciliation snapshot. The Safe balance covers this correction. The whole batch was simulated in Safe context and all **140 transfers succeeded**. Owner signatures, nonce and transaction guards still undergo your normal Safe checks. No on-chain state was changed by simulation.

Import the active file, review its scope, total and recipient count, and execute it once. Then run the fixed software from **v5 epoch 2851** using your regular payout process.

[Detailed audit and missing-checkpoint list](./v5-reconciliation-0-2850.audit.json) · [Verification](./v5-reconciliation-0-2850.verification.json) · [Compressed v5-only evidence](./v5-reconciliation-0-2850.evidence.json.gz)

Safe SHA-256: `6269e2fe3081f54ba84d4e20f0497ae31815964ea77bbb3088e99267c5bf3fe1`.
