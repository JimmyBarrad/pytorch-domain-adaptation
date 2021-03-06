# pytorch-domain-adaptation

This is an unofficial pytorch implementation of algorithms for domain adaptation.

**Note that this is an ongoing project and I cannot fully reproduce the results. Suggestions are welcome!**

## List of algorithms
- From source to target and back: symmetric bi-directional adaptive GAN [Russo+, CVPR2018].
- Augmented Cyclic Adversarial Learning for Domain Adaptation [Hosseini-Asl+, arXiv2018].

## Requirements
- Python 3.5+
- PyTorch 0.4
- TorchVision
- TensorboardX
- batchup
- click

## Usage

These examples are for the MNIST to USPS experiment.

### Train `Source Only` Model
```
CUDA_VISIBLE_DEVICES=<gpu_id> python train_classifier.py --exp mnist_usps --train_type unsup
```

### Train `Target Only` Model
```
CUDA_VISIBLE_DEVICES=<gpu_id> python train_classifier.py --exp mnist_usps --train_type sup
```

### Train Model
```
UDA_VISIBLE_DEVICES=<gpu_id> python test_classifier.py --exp mnist_usps --snapshot <snapshot_dir>
```
