# CrossTL translation matrix: HIP to Metal

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native HIP probe whose feature Metal has too straight to Metal, and metal checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.6 %: 259 supported, 0 refused, 1 wrong, 0 untested.

## Gaps

<details>
<summary>1 gaps: 0 refused, 1 wrong</summary>

Wrong, by cause:

- `the translation loses Decoration.Restrict`: `restrict-buffer`

</details>
