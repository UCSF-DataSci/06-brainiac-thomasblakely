[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vZAFH0Yf)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=22640707)
# Assignment 6: Neural Network Showdown

Build and compare neural network architectures on image and time-series data using Keras.

## Datasets

### CIFAR-10 (Parts 1 & 2)

60,000 color images (32x32 pixels) across 10 categories:

| Label | Category |
|:---:|:---|
| 0 | airplane |
| 1 | automobile |
| 2 | bird |
| 3 | cat |
| 4 | deer |
| 5 | dog |
| 6 | frog |
| 7 | horse |
| 8 | ship |
| 9 | truck |

### ECG5000 (Part 3)

5,000 heartbeat recordings (140 time steps each) across 5 categories:

| Label | Category |
|:---:|:---|
| 0 | Normal |
| 1 | Supraventricular |
| 2 | Premature Ventricular |
| 3 | Fusion |
| 4 | Unknown |

## Learning Objectives

- Build neural networks using Keras Sequential API
- Apply Dense, Conv2D, and LSTM layers to different data types
- Use callbacks (EarlyStopping, ModelCheckpoint) to manage training
- Evaluate models with accuracy and confusion matrices
- Compare architectures and understand when each is appropriate

## Setup

```bash
pip install -r requirements.txt
```

## Your Tasks

Complete the TODO cells in `assignment.ipynb` (or `assignment.md`). The notebook has three parts:

### Part 1: Dense Baseline on CIFAR-10

Build a Dense (fully connected) network. This baseline ignores spatial structure.

**Output:** `output/part1_results.json`

### Part 2: CNN on CIFAR-10

Build a CNN. Compare its accuracy to the Dense baseline.

**Outputs:**
- `output/part2_results.json`
- `output/part2_comparison.csv`
- `output/part2_training_history.png`

### Part 3: LSTM on ECG5000

Build an LSTM to classify heartbeat recordings.

**Outputs:**
- `output/part3_results.json`
- `output/part3_training_history.png`

## Running Your Code

```bash
jupytext --to notebook assignment.md
jupyter nbconvert --execute assignment.ipynb
```

Or open `assignment.ipynb` in Jupyter/VS Code and run cells interactively.

## Checking Your Work

```bash
pytest .github/tests/ -v
```

## Output Files Summary

| File | Part | Description |
|:---|:---:|:---|
| `part1_results.json` | 1 | Dense model accuracy and confusion matrix |
| `part2_results.json` | 2 | CNN accuracy and confusion matrix |
| `part2_comparison.csv` | 2 | Dense vs CNN accuracy comparison |
| `part2_training_history.png` | 2 | CNN training/validation curves |
| `part3_results.json` | 3 | LSTM accuracy and confusion matrix |
| `part3_training_history.png` | 3 | LSTM training/validation curves |

## Hints

See [hints.md](hints.md) if you get stuck.
