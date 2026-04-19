# Self-Pruning Neural Network using Learnable Gates

## Why L1 Penalty Encourages Sparsity

The L1 penalty encourages sparsity because it penalizes non-zero gate values linearly. When this penalty is applied to the sigmoid gates, the optimizer is pushed to reduce unnecessary gates toward zero. As a result, unimportant weights are effectively turned off and the network learns pruning during training.

Unlike L2 regularization, which mainly shrinks values smoothly, L1 creates stronger pressure for sparse solutions, making it a natural fit for weight pruning.

## Results

Dataset used for this run: `FakeData (2048 train / 512 test)`

| Lambda | Test Accuracy (%) | Sparsity (%) |
| --- | ---: | ---: |
| 1e-05 | 12.50 | 0.00 |
| 1e-04 | 12.50 | 0.00 |
| 1e-03 | 12.50 | 0.00 |

## Gate Distribution

The saved plot in `gate_distribution.png` shows the learned gate distribution after training the best-performing model. A useful pruning outcome typically shows many gates concentrated near 0 while keeping another group away from 0 for the connections the model still relies on.
