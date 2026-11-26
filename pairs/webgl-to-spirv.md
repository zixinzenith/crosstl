# CrossTL translation matrix: WebGL to SPIR-V

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native WebGL probe whose feature SPIR-V has too straight to SPIR-V, and spirv-val checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.7 %: 296 supported, 1 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>1 gaps: 1 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.vulkan-lowering-unsupported: SpirvLoweringRefused: SPIR-V cannot lower N construct: Unknown variable gl_ViewID_OVR (target vulkan) [project.translate.vulkan-lowering-unsupported]`: `view-index`

</details>
