# CrossTL translation matrix: WebGL to Slang

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native WebGL probe whose feature Slang has too straight to Slang, and slangc checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.6 %: 265 supported, 0 refused, 1 wrong, 0 untested.

## Gaps

<details>
<summary>1 gaps: 0 refused, 1 wrong</summary>

Wrong, by cause:

- `error[E30015]: undefined identifier 'gl_ViewID_OVR'`: `view-index`

</details>
