# CNN Classifier

Image classification on **CIFAR-10** using a custom Convolutional Neural Network (CNN) and a modified ResNet-18 implemented in PyTorch.

## Models

- **Custom CNN:** Three convolutional blocks with batch normalization, max pooling, dropout, and adaptive average pooling.
- **Modified ResNet-18:** An 18-layer residual network adapted for small images:
  - Uses **3 × 3 convolution filters** in the initial layer instead of 7 × 7.
  - Removes the initial max-pooling layer to preserve spatial information.
  - Uses residual connections to facilitate training a deeper network.

## Training Configuration

The notebooks use the following core training settings:

| Parameter | Value |
|---|---|
| Batch size | 128 |
| Epochs | 20 |
| Optimizer | Adam |
| Initial learning rate / maximum scheduler rate | 0.001 |
| Weight decay | 0.0005 |
| Loss function | Cross-entropy |
| Learning-rate scheduler | OneCycleLR |

## Performance Comparison

| Metric | Custom CNN | Modified ResNet-18 |
|---|---:|---:|
| Dataset | CIFAR-10 | CIFAR-10 |
| Epochs | 20 | 20 |
| Training Accuracy | 77.06% | 97.39% |
| Test Accuracy | 78.41% | 92.87% |

**Result:** Modified ResNet-18 achieves **14.46 percentage points higher test accuracy** than the custom CNN in the recorded experiments.

## Tech Stack

- Python
- PyTorch and Torchvision
- NumPy and Matplotlib
- Jupyter Notebook

## License

This project is licensed under the MIT License.
