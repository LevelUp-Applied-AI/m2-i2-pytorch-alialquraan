[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/YUvA8hIt)
# Integration 2 — PyTorch: Housing Price Prediction

**Module 2 — Programming for AI & Data Science**

See the [Module 2 Integration Task Guide](https://levelup-applied-ai.github.io/aispire-14005-pages/modules/module-2/learner/integration-guide) for full instructions.

---

## Quick Reference

**File to complete:** `train.py`

**Install PyTorch before running:**
```bash
pip install torch --index-url https://download.pytorch.org/whl/cpu
```

**Branch:** `integration-2/pytorch`

**Submit:** PR URL → TalentLMS Unit 8 text field

# Module 2 — Integration Task: PyTorch Housing Price Prediction

## 1. Model Description
This model is designed to predict housing prices in Jordan based on five key features:
* `area_sqm`: Apartment area.
* `bedrooms`: Number of bedrooms.
* `floor`: Floor level.
* `age_years`: Building age.
* `distance_to_center_km`: Distance to the city center.

The model predicts a single continuous value: `price_jod` (Target Variable).

## 2. Training Configuration
* **Architecture**: Neural Network with two linear layers.
    * Input Layer: 5 features -> 32 hidden units.
    * Activation: ReLU.
    * Output Layer: 32 units -> 1 price output.
* **Epochs**: 100
* **Learning Rate**: 0.01
* **Optimizer**: Adam
* **Loss Function**: Mean Squared Error (MSELoss)

## 3. Training Outcome
The model was trained for 100 epochs. The loss successfully decreased during the training process:
* **Initial Loss (Epoch 10)**: 1,950,493,184.00
* **Mid-way Loss (Epoch 50)**: 1,949,026,176.00
* **Final Loss (Epoch 100)**: 1,942,870,784.00

The final predictions were saved to `predictions.csv`.

## 4. Behavioral Observation
The loss decreased consistently throughout the 100 epochs, but it decreased at a slow rate. This suggests that the model might benefit from more training epochs or further tuning of the learning rate to reach a better global minimum.