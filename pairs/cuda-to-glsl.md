# CrossTL translation matrix: CUDA to GLSL

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native CUDA probe whose feature GLSL has too straight to GLSL, and glslangValidator checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 98.9 %: 273 supported, 3 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>3 gaps: 3 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.opengl-builtin-operand-unsupported: OpenGLBuiltinOperandError: OpenGL cannot translate 'tan' of double: GLSL declares it for N-bit floating-point operands only (GLSL N.N sections N.N and N.N), and converting a N-bit operand would change its range and precision`: `tan`
- `project.translate.rule-inexpressible: RuleInexpressibleError: __cgl_libm_cos on a N-bit floating-point operand has no helper for opengl: the helper takes binary32 values only (target opengl) [project.translate.rule-inexpressible]`: `cos`
- `project.translate.rule-inexpressible: RuleInexpressibleError: __cgl_libm_sin on a N-bit floating-point operand has no helper for opengl: the helper takes binary32 values only (target opengl) [project.translate.rule-inexpressible]`: `sin`

</details>
