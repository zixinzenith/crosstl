# CrossTL translation matrix: WebGL to Rust

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native WebGL probe whose feature Rust has too straight to Rust, and rust-gpu checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 96.8 %: 245 supported, 7 refused, 1 wrong, 0 untested.

## Gaps

<details>
<summary>8 gaps: 7 refused, 1 wrong</summary>

Wrong, by cause:

- `[VUID-StandaloneSpirv-OpEntryPoint-N] Entry-point has conflicting output location assignment at location N, component N`: `multiple-render-targets`

Refused, by diagnostic:

- `project.translate.rust-lowering-unsupported: RustLoweringRefused: Rust cannot lower N construct: texture operation: '<feature>' reads with a texel offset, and spirv-std's image operands have no Offset (target rust) [project.translate.rust-lowering-unsupported]` (3): `textureGradOffset`, `textureLodOffset`, `textureOffset`
- `project.translate.rust-lowering-unsupported: RustLoweringRefused: Rust cannot lower N construct: built-in: 'gl_ViewID_OVR' is used by name, and the rust-gpu output binds no entry-point parameter for it (target rust) [project.translate.rust-lowering-unsupported]`: `view-index`
- `project.translate.rust-lowering-unsupported: RustLoweringRefused: Rust cannot lower N construct: function: 'matrixCompMult' has no rust-gpu lowering for these operands (target rust) [project.translate.rust-lowering-unsupported]`: `matrixCompMult`
- `project.translate.rust-lowering-unsupported: RustLoweringRefused: Rust cannot lower N constructs: function: 'equal' has no rust-gpu lowering for these operands; function: 'notEqual' has no rust-gpu lowering for these operands; function: 'any' has no rust-gpu lowering for these operands (target rust) [project.translate.rust-lowering-unsupported]`: `bool-vector-logic`
- `project.translate.rust-refused: RustRefusal: type: glam has no 2x3 matrix of f32 (Mat2x3<f32>); rust-gpu shaders have square f32 and f64 matrices`: `matrix-resize`

</details>
