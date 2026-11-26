# CrossTL translation matrix: SPIR-V to GLSL

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native SPIR-V probe whose feature GLSL has too straight to GLSL, and glslangValidator checked the result. Its compute probes also ran on a runtime. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 99.8 %: 509 supported, 1 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>1 gaps: 1 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.opengl-refused: OpenGLRefusal: OpenGL texture operation 'textureLod' requires a declared texture or image resource argument: FunctionCallNode(function=IdentifierNode(name=nonuniformEXT), arguments=N)`: `array-of-textures-nonuniform-index`

</details>
