### Table 7. Overall performance under original and CRPS-based routing

`S` denotes the original `sMAPE`-based routing, and `C` denotes the new `CRPS`-based routing. Lower values are better.

| Metric | S-Top1 | C-Top1 | S-Top3 | C-Top3 | S-Top5 | C-Top5 |
| :----- | :----: | :----: | :----: | :----: | :----: | :----: |
| sMAPE  | 0.437  | 0.444  | 0.436  | 0.438  | 0.437  | 0.436  |
| MASE   | 1.570  | 1.536  | 1.560  | 1.542  | 1.557  | 1.545  |
| CRPS   | 0.243  | 0.229  | 0.213  | 0.215  | 0.213  | 0.212  |
| Rank   | 3.412  | 3.701  | 2.886  | 3.071  | 2.721  | 2.866  |

This supports two key messages:

1. **ZooCast can be naturally extended to probabilistic forecasting.**  
   Once the selector operates on distributions rather than point predictions, and $E$ is built with `CRPS`, the same selection-and-ensemble pipeline can support probabilistic outputs.

2. **Even though the advantage subsets change substantially under `CRPS`, downstream performance remains stable.**  
   This indicates that the later ECOC and weighting stages provide important robustness, consistent with Table 3 in the paper.