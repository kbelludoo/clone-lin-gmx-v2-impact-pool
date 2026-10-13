# clone-lin-gmx-v2-impact-pool

Experimental LIN clone of GMX V2 `capPositiveImpactUsdByPositionImpactPool` / `getMaxLendableUsdAvailable` (uint64-scale, FLOAT' = 1e6).

- **Upstream:** [gmx-io/gmx-synthetics](https://github.com/gmx-io/gmx-synthetics) `contracts/market/MarketUtils.sol` commit `a85ea3491c19c93bb4b5a002d9b358fb769b7849` (GPL-2.0-or-later after BUSL Change Date 2026-08-31).
- **LIN kernel:** [`src/lin_gmx_v2_impact_pool.lin`](src/lin_gmx_v2_impact_pool.lin)
- **Proofs (lin-open only):** [kbelludoo/lin-open](https://github.com/kbelludoo/lin-open) `examples/gmx_v2_impact_pool/` and `python3 test/prove_gmx_v2_impact_pool_external.py`
- **Class:** EXPERIMENTAL. Not Arbitrum GMX V2 uint256 / FLOAT=1e30. Not a production replacement.

Named goldens (uint64-scale): clip **150000000** vs uncapped **200000000** vs pool-only **100000000** vs sizeDelta **50000000**; config min **140000000** vs noconfig **200000000**; lent consume **120000000** vs nolent **200000000**; over-lent **100000000**; negative passthrough **-200000000** vs symmetric abs **-150000000**; factor 0 **100000000** vs stay **200000000**; long-only **125000000**; 128-bit wrap **14000000000000** vs naive i64 **-4446744073709**.
