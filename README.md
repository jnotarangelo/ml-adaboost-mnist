# AdaBoost on MNIST: Boosting, Saliency Maps and Embeddings

This repository contains our solution to the second assignment (DM 2) of our **Machine Learning course**. This is a **group project**, carried out jointly as part of the course curriculum.

## Goal

The objective of this project is threefold:

1. **Boosting for digit recognition**: apply the AdaBoost algorithm to the MNIST dataset (28×28 grayscale images of handwritten digits) by varying:
  - the weak learners: decision stumps, perceptrons, and decision trees of different depths;
  - the number of boosting steps;
  - the binary classification tasks (e.g. digit `3` vs. digit `8`, or digits `0–4` vs. digits `5–9`).
2. **Saliency maps**: build saliency maps from the learned models. Since each decision stump tests a single pixel, the pixels examined by the stumps directly highlight the regions of the image that drive the decision.
3. **Embedding**: learn a low-dimensional embedding by training a one-hidden-layer MLP auto-associator on the images (with N ≪ 784, e.g. N = 64), then repeat the boosting experiments in this new input space and compute backpropagated saliency maps in pixel space (GradCAM-style).

> Note: no PCA dimensionality reduction is used in these experiments.

## Results

- Confusion matrices are reported for each combination of parameters, together with an analysis of the most and least favorable configurations.
- Saliency maps are provided for several parameter combinations, mainly for binary discriminations between two digits, where they are easier to interpret.
- Experiments are then repeated in the learned embedding space and compared with the original pixel space.

## Team

This project was completed as a group exercise for our Machine Learning course.

## References

- [MNIST dataset](http://yann.lecun.com/exdb/mnist/)
- [Unleashing the Power of Ensemble Methods: A Deep Dive into Classification Using the MNIST Dataset](https://medium.com/@nik.avgeros/unleashing-the-power-of-ensemble-methods-a-deep-dive-into-classification-using-the-mnist-dataset-1aeefab4c6a6)
- Freund, Y., &amp; Schapire, R. E. (1997). *A Decision-Theoretic Generalization of On-Line Learning and an Application to Boosting.*