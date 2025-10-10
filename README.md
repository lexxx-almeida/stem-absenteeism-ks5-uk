**Objective**: Predict protein expression directly from histology image patches (train/val on B1, C1, D1; hold out A1 for final test).

**Scope**:<br/>
**Single-target**: CD11b protein only.<br/>
**Multi-target**: all proteins with specimen-aware validation (LOSO/GroupKFold).

**Metrics**: RMSE, R², Pearson (ρ), Spearman (ρₛ).

| Model                  |    RMSE   |     R²    | ρ (Pearson) | ρₛ (Spearman) |
| ---------------------- | :-------: | :-------: | :---------: | :-----------: |
| OLS Regression         |   1.298   |   0.220   |    0.470    |     0.534     |
| Random Forest          | **1.033** | **0.506** |  **0.714**  |   **0.712**   |
| SVR                    |   1.079   |   0.461   |    0.685    |     0.695     |
| **Single-Protein CNN** | **0.173** | **0.986** |  **0.999**  |   **0.998**   |

<img width="1789" height="490" alt="11_ScatterPlots" src="https://github.com/user-attachments/assets/2b4205ac-25aa-439d-a6ec-efde573fd17b" />

<img width="685" height="545" alt="12_ScatterTrue_Predicted" src="https://github.com/user-attachments/assets/eacb5123-06d0-4780-a850-4a6b183077f5" />
