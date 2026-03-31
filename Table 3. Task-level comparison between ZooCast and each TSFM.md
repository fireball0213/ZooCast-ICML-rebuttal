### Table 3. Task-level comparison between ZooCast and each TSFM

For each TSFM, this table reports how often ZooCast wins, ties, or loses across tasks, together with the number of tasks on which that TSFM is the best single model. Higher `ZooCast Outperform Rate` indicates that ZooCast is not simply filtering weak models.

|                             | Moi.S  | Chr.bT |  Toto  | Moi2.S | Flo.r1 | Kai.10 | TFM.25 | TiRex  | Chr.2  |
| :-------------------------- | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Best-Model Count (`sMAPE`)  |   0    |   7    |   1    |   10   |   12   |   30   |   6    |   14   |   17   |
| Best-Model Count (`MASE`)   |   1    |   7    |   5    |   17   |   13   |   2    |   6    |   24   |   22   |
| ZooCast Win                 |   89   |   81   |   81   |   68   |   62   |   49   |   76   |   48   |   51   |
| ZooCast Tie                 |   5    |   6    |   6    |   13   |   9    |   15   |   3    |   11   |   29   |
| ZooCast Loss                |   3    |   10   |   10   |   16   |   26   |   33   |   18   |   38   |   17   |
| **ZooCast Outperform Rate** | 96.91% | 89.69% | 89.69% | 83.51% | 73.20% | 65.98% | 81.44% | 60.82% | 82.47% |

This result supports two key points:

1. ZooCast is **not** a simple weak-model filter. Its task-level comparison pattern echoes the oracle heterogeneity in which different models are best on different tasks, and the `Tie` distribution also broadly follows the best-model structure. This indicates that the gain comes from task-dependent dynamic ranking, rather than mechanically favoring a few globally strong models.

2. The practical gain is therefore not merely an artifact of aggregated `Rank`, because the gain is also visible directly at the task level through consistent win/tie/loss statistics.