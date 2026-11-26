# CrossTL translation matrix: SPIR-V to HIP

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native SPIR-V probe whose feature HIP has too straight to HIP, and hipcc checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 100.0 %: 250 supported, 0 refused, 0 wrong, 2 untested.

## Gaps

<details>
<summary>2 untested: type 2</summary>

- `slangc or spirv-dis is not installed` (2): `pointer-arithmetic`, `pointer-local`

</details>
