### Table 5. Static ensembles vs ZooCast-guided ensembles

This table compares ZooCast-guided Top-K ensembles with hindsight-selected static Top-3 and Top-5 committees. Lower is better. **Bold** marks the best result in each row, and `code` marks the second best.

| Domain                 | Metric | Current_best_3 En. | Current_best_5 En. | ZooCast-Top3 En. | ZooCast-Top5 En. |
| :--------------------- | :----: | :----------------: | :----------------: | :--------------: | :--------------: |
| Econ/Fin (n=6)         |  MASE  |      `1.845`       |     **1.825**      |      1.872       |      1.853       |
|                        |  Rank  |      `2.000`       |     **1.833**      |      2.333       |     `2.000`      |
| Energy (n=32)          |  MASE  |       1.054        |      `1.053`       |     `1.053`      |    **1.052**     |
|                        |  Rank  |      `2.969`       |     **2.875**      |      3.281       |      3.062       |
| Healthcare (n=5)       |  MASE  |       7.653        |       7.611        |    **7.417**     |     `7.468`      |
|                        |  Rank  |        3.8         |       3.400        |    **3.000**     |     `3.200`      |
| Nature (n=15)          |  MASE  |       1.045        |      `1.041`       |      1.052       |    **1.037**     |
|                        |  Rank  |      `2.867`       |     **2.733**      |      3.733       |      3.000       |
| Sales (n=4)            |  MASE  |       0.757        |       0.752        |    **0.740**     |     `0.742`      |
|                        |  Rank  |       `2.5`        |     **2.000**      |      4.750       |      3.750       |
| Transport (n=15)       |  MASE  |       0.753        |       0.744        |     `0.742`      |    **0.741**     |
|                        |  Rank  |       3.133        |      `1.867`       |     `1.867`      |    **1.800**     |
| Web/CloudOps (n=20)    |  MASE  |       2.146        |       2.048        |    **1.916**     |     `1.962`      |
|                        |  Rank  |        4.75        |       5.200        |    **3.250**     |     `3.450`      |
| **ALL Domains (n=97)** |  MASE  |       1.608        |       1.582        |     `1.560`      |    **1.557**     |
|                        |  Rank  |       3.309        |       3.103        |     `2.886`      |    **2.721**     |

This comparison supports three main conclusions:

1. On the global result, ZooCast **still outperforms** the strongest static ensembles. On `ALL Domains`, both `ZooCast-Top3` and `ZooCast-Top5` achieve better `MASE` and `Rank` than `Current_best_3/5`, so the improvement is unlikely to be explained solely by removing weak models.
2. Even when `k=5`, dynamic ranking still matters. While `Top-5` reflects substantial ensemble complementarity in the current zoo, the table shows that a fixed hindsight-selected strongest committee remains weaker than ZooCast. This suggests that the gain comes not only from choosing strong models, but also from changing the ranking and composition according to the task.
3. The strongest static ensemble itself depends on post hoc global screening. It requires exhaustive evaluation to identify which models are "currently strongest", whereas ZooCast aims to recover a near-optimal task-specific ranking without full evaluation.