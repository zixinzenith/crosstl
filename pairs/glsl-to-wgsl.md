# CrossTL translation matrix: GLSL to WGSL

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native GLSL probe whose feature WGSL has too straight to WGSL, and naga checked the result. Its compute probes also ran on a runtime. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 97.5 %: 357 supported, 1 refused, 8 wrong, 1 untested.

## Gaps

<details>
<summary>9 gaps: 1 refused, 8 wrong</summary>

Wrong, by cause:

- `no definition in scope for identifier: '<feature>'` (5): `front-facing`, `instance-index`, `primitive-id`, `sample-index`, `vertex-index`
- `on vulkan-lavapipe as SPIR-V from glslangValidator and naga, the translation computes different results from the native probe` (3): `buffer-row-major-array`, `buffer-row-major-matrix`, `buffer-row-major-non-square`

Refused, by diagnostic:

- `project.translate.wgsl-refused: WGSLRefusal: WGSL target does not support CrossGL resource type image2DMS yet; split texture/sampler/storage bindings are required`: `imageSamples`

</details>

<details>
<summary>1 untested: function 1</summary>

- `the target's own probe is rejected: error: no definition in scope for identifier: 'subgroupElect'`: `subgroupElect`

</details>
