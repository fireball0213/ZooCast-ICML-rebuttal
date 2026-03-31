### Table 8. Leave-one-domain-out robustness of the representation set $\mathcal{D}$

Starting from the full 7-domain setting, we remove one domain at a time from $\mathcal{D}$ so that the target domain is completely absent from the representation pool. We then report the affected target-domain performance together with the overall `DomainMean`. Larger changes indicate higher sensitivity to the missing domain.

| Config           | Econ/Fin | Energy | Healthcare | Nature |  Sales | Transport | Web/CloudOps | DomainMean |
| :--------------- | -------: | -----: | ---------: | -----: | -----: | --------: | -----------: | ---------: |
| Full domain      |   0.0928 | 0.4636 |     0.1194 | 0.6059 | 0.9345 |    0.1982 |       0.5313 |     0.4208 |
| w/o Econ/Fin     |   0.0966 |      - |          - |      - |      - |         - |            - |     0.4170 |
| w/o Energy       |        - | 0.4596 |          - |      - |      - |         - |            - |     0.4140 |
| w/o Healthcare   |        - |      - |     0.1230 |      - |      - |         - |            - |     0.4202 |
| w/o Nature       |        - |      - |          - | 0.5540 |      - |         - |            - |     0.4152 |
| w/o Sales        |        - |      - |          - |      - | 0.9477 |         - |            - |     0.4272 |
| w/o Transport    |        - |      - |          - |      - |      - |    0.1989 |            - |     0.4201 |
| w/o Web/CloudOps |        - |      - |          - |      - |      - |         - |       0.5614 |     0.4407 |

This result supports two points:

1. **ZooCast is relatively robust on most domains.**  
   Removing most domain causes only limited changes on the corresponding target domain, and only small changes in DomainMean.

2. **Sensitivity mainly appears for highly distinctive domains.**  
   Removing `Web/CloudOps` causes the clearest degradation on the corresponding target domain and the largest drop in DomainMean. This suggests that when a highly distinctive domain is completely absent from $\mathcal{D}$, recommendation quality can decline.