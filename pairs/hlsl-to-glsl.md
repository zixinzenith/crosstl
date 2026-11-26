# CrossTL translation matrix: HLSL to GLSL

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native HLSL probe whose feature GLSL has too straight to GLSL, and glslangValidator checked the result. Its compute probes also ran on a runtime. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.8 %: 443 supported, 0 refused, 1 wrong, 0 untested.

## Gaps

<details>
<summary>1 gaps: 0 refused, 1 wrong</summary>

Wrong, by cause:

- `on vulkan-lavapipe as SPIR-V from dxc and glslangValidator, the translation computes different results from the native probe`: `cross`

</details>
