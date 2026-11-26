# CrossTL translation matrix: GLSL to SPIR-V

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native GLSL probe whose feature SPIR-V has too straight to SPIR-V, and spirv-val checked the result. Its compute probes also ran on a runtime. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.2 %: 522 supported, 4 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>4 gaps: 4 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.vulkan-builtin-unsupported: SPIRVBuiltinLoweringError: Cannot lower call to 'interpolate_at_centroid' to SPIR-V: it is neither a declared function nor a built-in with a SPIR-V lowering`: `interpolateAtCentroid`
- `project.translate.vulkan-builtin-unsupported: SPIRVBuiltinLoweringError: Cannot lower call to 'interpolate_at_offset' to SPIR-V: it is neither a declared function nor a built-in with a SPIR-V lowering`: `interpolateAtOffset`
- `project.translate.vulkan-builtin-unsupported: SPIRVBuiltinLoweringError: Cannot lower call to 'interpolate_at_sample' to SPIR-V: it is neither a declared function nor a built-in with a SPIR-V lowering`: `interpolateAtSample`
- `project.translate.vulkan-lowering-unsupported: SpirvLoweringRefused: SPIR-V cannot lower N construct: cannot assign to undeclared variable gl_FragStencilRefARB (target vulkan) [project.translate.vulkan-lowering-unsupported]`: `stencil-export`

</details>
