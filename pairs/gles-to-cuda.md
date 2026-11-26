# CrossTL translation matrix: GLSL ES to CUDA

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native GLSL ES probe whose feature CUDA has too straight to CUDA, and nvcc checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 100.0 %: 238 supported, 0 refused, 0 wrong, 2 untested.

## Gaps

<details>
<summary>2 untested: type 2</summary>

- `untested in the gles input row: the probe itself is rejected: ERROR: 0:10: '64-bit integer' : not supported with this profile: es`: `int64`
- `untested in the gles input row: the probe itself is rejected: ERROR: 0:10: '64-bit unsigned integer' : not supported with this profile: es`: `uint64`

</details>
