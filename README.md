# CIFAR-10 with a small CNN in PyTorch

> Course assignment from 2023, kept as it was written. The notes under "Reading the result" were added in November 2026.

A first convolutional network in PyTorch: load CIFAR-10 with torchvision, hold out 20% of the
training set for validation, train with SGD and report accuracy per class.

## Result

Test accuracy **62%** (6,216 of 10,000 images).

| Class | Accuracy | Class | Accuracy |
|---|---|---|---|
| automobile | 78% | airplane | 65% |
| frog | 70% | horse | 64% |
| ship | 70% | bird | 60% |
| truck | 67% | dog | 54% |
| deer | 47% | cat | 42% |

## Reading the result

- 62% is what a small network without augmentation or batch normalisation reaches. A ResNet-18
  with standard augmentation passes 93% on the same data.
- Cat (42%), deer (47%) and dog (54%) are the weak classes.
- The cell that prints the loss sits outside the training loop, so the notebook shows one epoch
  line instead of the full curve.

## Newer work on the same topic

- [autograd-from-scratch](https://github.com/faiqrasulov/autograd-from-scratch): the same kind of CNN trained on an autodiff engine written in NumPy and checked against PyTorch.

## Files

| File | Content |
|---|---|
| `CIFAR-10_CNN.ipynb` | Notebook (the data is downloaded by torchvision) |
| `CIFAR-10_CNN.html` | Rendered copy |
| `About.txt` | Original brief |
