# CrossTL translation matrix: CUDA to SPIR-V

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native CUDA probe whose feature SPIR-V has too straight to SPIR-V, and spirv-val checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 96.9 %: 279 supported, 9 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>9 gaps: 9 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.vulkan-builtin-unsupported: SPIRVBuiltinLoweringError: Cannot lower call to '<feature>' to SPIR-V: <feature> requires N-bit floating-point scalar or vector operand` (7): `ceil`, `floor`, `rint`, `rsqrt`, `sqrt`, `tan`, `trunc`
- `project.translate.rule-inexpressible: RuleInexpressibleError: __cgl_libm_cos on a N-bit floating-point operand has no helper for vulkan: the helper takes binary32 values only (target vulkan) [project.translate.rule-inexpressible]`: `cos`
- `project.translate.rule-inexpressible: RuleInexpressibleError: __cgl_libm_sin on a N-bit floating-point operand has no helper for vulkan: the helper takes binary32 values only (target vulkan) [project.translate.rule-inexpressible]`: `sin`

</details>
