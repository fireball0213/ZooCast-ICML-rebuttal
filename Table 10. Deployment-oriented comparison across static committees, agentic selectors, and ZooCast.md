

### $\underline{\text{Table  10: Deployment-oriented comparison across static committees, agentic selectors, and ZooCast}}$

| Method                     | Core target                        | Selection basis                                              | Requires task-time forward / CV | Incremental update when new models arrive | Growing-zoo readiness | Main limitation                                              |
| :------------------------- | :--------------------------------- | :----------------------------------------------------------- | :-----------------------------: | :---------------------------------------: | :-------------------: | :----------------------------------------------------------- |
| **Fixed strongest subset** | Strong static deployment policy    | Benchmark-guided global screening                            |              🟢 No               |                   🔴 No                    |        🔴 Weak         | The strongest subset must be refreshed externally and usually depends on lagged benchmark evidence |
| **Latest model**           | Simplest deployment heuristic      | Release time only                                            |              🟢 No               |                   🟢 Yes                   |       🟡 Partial       | Ignores task heterogeneity and assumes “newer = better”      |
| **All-current ensemble**   | Hedge by averaging                 | Average all currently available models                       |              🔴 Yes              |                   🟢 Yes                   |       🟡 Partial       | Computationally expensive and not task-adaptive              |
| **TimeCopilot**            | Agentic forecasting workflow       | Feature analysis + model evaluation + cross-validation       |              🔴 Yes              |    🟡 Not designed as a reusable router    |        🔴 Weak         | Strong in workflow orchestration and explainability, but not designed for reusable routing under zoo growth |
| **MoiraiAgent**            | Context-aware expert selection     | Candidate predictions + short-lookback CV errors + context signals |              🔴 Yes              |                 🟡 Limited                 |        🔴 Weak         | Closer to task-time evaluation-based selection; main strength is context-aware forecasting |
| **ZooCast (ours)**         | Reusable routing for a growing zoo | Precomputed representation library + similarity routing      |              🟢 No               |                   ✅ Yes                   |       ✅ Strong        | Raw gain over the strongest static committees is modest, but it preserves incremental updating, few-window routing, and task adaptivity |

#### Legend

- 🟢 favorable / low burden / supported
- 🟡 partial / conditional
- 🔴 unfavorable / high burden / weak
- ✅ explicitly supported

#### Main takeaway

1. Strong static committees are reasonable baselines, but they are better viewed as externally maintained policies **rather than self-updating routing mechanisms**.  
2. TimeCopilot and MoiraiAgent confirm that model selection is becoming an important community focus, but they rely more on **LLM-driven orchestration** and **task-time evaluation-based routing**, respectively, rather than reusable and incrementally updatable routing under zoo growth.
3. ZooCast targets a different objective: not the highest static score on a fixed zoo, but sustained routing ability under growing-zoo evolution, few-window task representation, and no full-zoo refresh whenever new models arrive.