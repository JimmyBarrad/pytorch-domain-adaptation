# pytorch-SBADA-GAN

This is an unofficial pytorch implementation of a paper, From source to target and back: symmetric bi-directional adaptive GAN [Russo+, CVPR2018].

Please note that this is an ongoing project and I cannot fully reproduce the results currently.


## Requirements
- Python 3.5+
- PyTorch 0.3
- TorchVision
- TensorboardX
- batchup
- tqdm
- click


## Usage

These examples are for the MNIST to USPS experiment.

### Train `Source Only` Model
```
CUDA_VISIBLE_DEVICES=<gpu_id> python train_unsup.py --exp mnist_usps
```

### Train `Target Only` Model
```
CUDA_VISIBLE_DEVICES=<gpu_id> python train_sup.py --exp mnist_usps
```

### Train SBADA-GAN Model
```
CUDA_VISIBLE_DEVICES=<gpu_id> python train_sbada_gan.py --exp mnist_usps
```

## Results
Accuracy [%] is shown. Note that the values are slightly different from the original paper [1].

| | MNIST->USPS | USPS->MNIST | SVHN->MNIST | MNIST->SVHN |
:---:|:----:|:----:|:----:|:----: 
| Source Only |  |  |  |  |
| Target Only |  |  |  |  |

## References
- [1]: R. Paolo et al. "From source to target and back: symmetric bi-directional adaptive GAN.", in CVPR, 2018.
