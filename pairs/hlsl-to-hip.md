# CrossTL translation matrix: HLSL to HIP

Measured on commit [`d698cde`](https://github.com/CrossGL/crosstl/commit/d698cde012f05b2329600c69dbcac6634b78bc09) at 2026-11-26T11:11:45Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native HLSL probe whose feature HIP has too straight to HIP, and hipcc checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 98.8 %: 238 supported, 3 refused, 0 wrong, 0 untested.

## Gaps

<details>
<summary>3 gaps: 3 refused, 0 wrong</summary>

Refused, by diagnostic:

- `project.translate.hip-lowering-unsupported: HipLoweringRefused: HIP cannot lower N construct: HIP structured buffer atomic: atomicCompSwap on RWStructuredBuffer<float> requires supported scalar int/uint target (target hip) [project.translate.hip-lowering-unsupported]` (2): `InterlockedCompareExchangeFloatBitwise`, `InterlockedCompareStoreFloatBitwise`
- `project.translate.hip-lowering-unsupported: HipLoweringRefused: HIP cannot lower N construct: HIP imageStore on storage image 'img': @texel(unorm, vec4) leaves the size of a texel to the bound view, which a surface does not have (target hip) [project.translate.hip-lowering-unsupported]`: `unorm-storage-image`

</details>
