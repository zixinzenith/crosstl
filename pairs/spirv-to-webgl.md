# CrossTL translation matrix: SPIR-V to WebGL

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native SPIR-V probe whose feature WebGL has too straight to WebGL, and glslangValidator checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 75.0 %: 15 supported, 5 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>5 gaps: 5 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.webgl-lowering-unsupported: WebGLLoweringRefused: WebGL cannot lower N construct: WebGL target does not support storage buffer resource '_' (RWStructuredBuffer) (target webgl) [project.translate.webgl-lowering-unsupported]` (5): `OpDPdx`, `OpDPdy`, `OpFwidth`, `OpImageSampleImplicitLod`, `OpImageSampleProjImplicitLod`

</details>
