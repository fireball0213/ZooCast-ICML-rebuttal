### Table 9. Representative assignment under different source pools

This table reports how many of the 3000 representatives are assigned to each TSFM when different source pools are used to build $\mathcal{D}$.

| Model  | Original | w/o $\mathcal{D}_{Chr}$ | w/o $\mathcal{D}_{Moi}$ |
| :----: | -------: | ----------------------: | ----------------------: |
| Moi.S  |      279 |                     324 |                     194 |
| Chr.bT |      293 |                     310 |                     367 |
|  Toto  |      209 |                     173 |                     219 |
| Moi2.S |      450 |                     432 |                     405 |
| Flo.r1 |      238 |                     206 |                     295 |
| Kai.10 |      278 |                     221 |                     328 |
| TFM.25 |      329 |                     268 |                     288 |
| TiRex  |      343 |                     394 |                     314 |
| Chr.2  |      581 |                     672 |                     590 |

This table does not suggest a simple same-family source bias toward Chronos or Moirai. Removing $\mathcal{D}_{Moi}$ only moderately reduces the subset sizes of `Moi.S` and `Moi2.S`, while removing $\mathcal{D}_{Chr}$ does not reduce `Chr.2` and even increases its assigned subset size. More broadly, this suggests that source overlap may not behave like simple same-source overfitting at TSFM pretraining scale, while a broader and more diverse source pool could still further improve fairness and robustness.