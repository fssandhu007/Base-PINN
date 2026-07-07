# Base-PINN

This project implements a Physics-Informed Neural Network (PINN) to predict fluid velocity fields while incorporating the governing laws of fluid mechanics directly into the learning process.

Unlike conventional neural networks that rely solely on data, this model combines supervised learning with physics-based constraints, enabling physically consistent predictions even with limited training data.

Physics Constraint:
The network learns the velocity components (u, v) from spatial-temporal coordinates (x, y, t) while minimizing both the prediction error and the residual of the incompressible continuity equation.
The model enforces the continuity equation for incompressible flow:
                      ∂x/∂u+∂y/∂v=0

This physics residual is added to the loss function to ensure that predictions satisfy conservation of mass.

Optimizer:
Adam Optimizer
Learning Rate = 0.001

Training: 
2000 epochs
Combined data loss + physics loss

Dataset Source:
Hugging Face Dataset: Allanatrix/CFD
