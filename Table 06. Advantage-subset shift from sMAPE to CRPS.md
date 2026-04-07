

### Table 6. Advantage-subset shift from sMAPE to CRPS

This table reports the size of each model's advantage subset under the two metrics and their overlap. Lower overlap indicates that the preferred regions change substantially when routing is made distribution-aware.

| Model  | Adv. size (`sMAPE`) | Adv. size (`CRPS`) | Overlap (`sMAPE`↔`CRPS`) |
| :----- | :-----------------: | :----------------: | :----------------------: |
| Moi.S  |         279         |        147         |          28.32%          |
| Chr.bT |         293         |        302         |          46.76%          |
| Toto   |         209         |        314         |          36.84%          |
| Moi2.S |         450         |        600         |          58.22%          |
| Flo.r1 |         238         |        261         |          45.38%          |
| Kai.10 |         278         |        235         |          34.53%          |
| TFM.25 |         329         |        345         |          47.42%          |
| TiRex  |         343         |        290         |          29.74%          |
| Chr.2  |         581         |        506         |          49.05%          |

This table shows that the routing structure changes substantially when the error matrix $E$ is switched from `sMAPE` to `CRPS`: across the 9 TSFMs, the average overlap is only **41.81%**. This indicates that the induced advantage subsets are metric-dependent, which is expected because point accuracy and distributional quality capture different aspects of predictive performance.