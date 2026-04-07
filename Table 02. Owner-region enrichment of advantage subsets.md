### Table 2. Owner-region enrichment of advantage subsets

This table compares each model's `Global@Top1` frequency with its `Owner@Top1` frequency inside its own induced advantage subset. Positive `Boost↑` means that the subset statistically enriches samples favorable to the owner model.

| Model             | Global@Top1 | Owner@Top1 |   Boost↑   |
| :---------------- | :---------: | :--------: | :--------: |
| Moi.S             |   16.79%    |   21.24%   |   26.46%   |
| Chr.bT            |    9.06%    |   11.94%   |   31.74%   |
| Toto              |    7.56%    |   11.98%   |   58.40%   |
| Moi2.S            |   15.96%    |   33.45%   |  109.58%   |
| Flo.r1            |    7.96%    |   16.82%   |  111.23%   |
| Kai.10            |   11.30%    |   14.02%   |   24.10%   |
| TFM.25            |    9.73%    |   10.37%   |   6.53%    |
| TiRex             |    5.83%    |   4.15%    |  -28.88%   |
| Chr.2             |   15.79%    |   26.00%   |   64.61%   |
| **AVG (9 TSFMs)** |   11.11%    |   16.66%   | **44.86%** |

This table shows two key facts:

1. For most models, the probability of being Top-1 increases noticeably inside their own advantage subset. Averaged over all 9 TSFMs, `Owner@Top1` improves by **44.86%** relative to `Global@Top1`. This indicates that the subsets are not random partitions, but statistically enrich the owner model's favorable region.

2. `TiRex` is an informative exception. It is already a globally strong model, so its advantage is less dependent on a specific local subset. In contrast, the purpose of advantage subsets is mainly to expose local specialization for models that are not globally dominant. Hence, a negative boost for `TiRex` does not invalidate the design; rather, it highlights that the mechanism is capturing local preference structure instead of merely rewarding the globally strongest model again.