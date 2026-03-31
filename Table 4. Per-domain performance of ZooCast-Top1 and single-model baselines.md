### Table 4. Per-domain performance of ZooCast-Top1 and single-model baselines

This table reports domain-level `MASE` and `Rank` for all single-model TSFMs and `ZooCast-Top1`. Lower is better. **Bold** marks the best result in each row, and `code` marks the second best.

| Domain                 | Metric | Moi.S |  Chr.bT   |  Toto   |  Moi2.S   | Flo.r1 |  Kai.10   | TFM.25  |   TiRex   |   Chr.2   | ZooCast-Top1 |
| :--------------------- | :----: | :---: | :-------: | :-----: | :-------: | :----: | :-------: | :-----: | :-------: | :-------: | :----------: |
| Econ/Fin (n=6)         |  MASE  | 2.385 |   2.013   |  2.159  |  `1.887`  | 1.906  |   1.962   |  2.020  | **1.885** |   1.923   |    1.894     |
|                        |  Rank  |  9.5  |   6.667   |  8.333  |     4     | 4.667  |   6.000   |  6.333  | **2.500** |   3.833   |   `3.167`    |
| Energy (n=32)          |  MASE  | 1.45  |   1.162   |  1.201  |   1.088   | 1.101  |   1.122   |  1.113  |  `1.074`  | **1.057** |    1.078     |
|                        |  Rank  | 9.531 |   6.000   |  7.719  |   5.344   | 5.156  |   4.156   |  5.719  |   4.125   |  `3.750`  |  **3.500**   |
| Healthcare (n=5)       |  MASE  | 7.486 |   8.855   | `7.357` |   7.952   | 7.493  |   8.887   |  8.226  |   7.400   |   7.620   |  **7.341**   |
|                        |  Rank  |  8.8  |   9.000   |   6.2   |     5     | 4.400  |   5.400   |  5.000  |  `4.000`  |   4.200   |  **3.000**   |
| Nature (n=15)          |  MASE  | 1.119 | **1.039** |  1.073  |   1.107   | 1.066  |   1.09    |  1.078  |  `1.055`  |   1.062   |    1.073     |
|                        |  Rank  | 8.067 |   4.133   |   7.6   |    7.8    | 4.867  | **3.000** |  6.467  |   4.067   |   5.200   |   `3.800`    |
| Sales (n=4)            |  MASE  | 0.793 |   0.769   |  0.765  |   0.753   | 0.763  |   0.79    | `0.749` |   0.749   | **0.747** |    0.759     |
|                        |  Rank  | 7.25  |   4.750   |   7.5   |     9     | 5.000  |  `4.000`  | `4.000` |   4.750   |   5.500   |  **3.250**   |
| Transport (n=15)       |  MASE  | 0.971 |   0.912   |  0.827  |   0.783   | 0.769  |   0.811   | `0.756` | **0.749** |   0.768   |    0.776     |
|                        |  Rank  |  8.6  |   8.533   |  6.867  |   6.733   | 4.733  |   6.200   | `3.067` | **2.133** |   3.467   |    4.667     |
| Web/CloudOps (n=20)    |  MASE  | 2.751 |   2.903   |  2.065  | **1.752** | 1.989  |   2.515   |  2.132  |   2.251   |   1.933   |   `1.932`    |
|                        |  Rank  |  7.7  |   7.800   |  5.55   |    3.8    | 6.750  |  `3.600`  |  6.600  |   5.800   |   4.000   |  **3.400**   |
| **ALL Domains (n=97)** |  MASE  | 1.935 |   1.897   |  1.655  |  `1.571`  | 1.593  |   1.795   |  1.670  |   1.626   |   1.573   |  **1.570**   |
|                        |  Rank  | 7.722 |   5.856   |  6.247  |   4.959   | 4.639  |   3.845   |  4.691  |   3.546   |  `3.495`  |  **3.412**   |

This table supports two conclusions. First, ZooCast-Top1 is not helped by only a few anomalous datasets: on **ALL Domains**, it achieves the best `MASE` and the best `Rank`, with gains also visible across multiple domains. Second, the fine-grained view is consistent with the aggregated conclusion: because the strongest single TSFM changes across domains, the relevant target is not to beat the oracle best model everywhere, but to maintain the best overall average behavior under such heterogeneity.