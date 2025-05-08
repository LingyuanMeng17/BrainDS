Less Data Better Performance: A Knowledge-Driven Semi-supervised Brain Analysis Method
================================================================

This is the code for BrainGS.

## Requirements

This code was developed and tested with Python 3.7.12, PyTorch 1.13.0, and PyG 2.1.0.
All dependencies are specified in the `requirements.txt` file.

## Usage

### Training Process

We provide a well-trained diffusion based graph generator in the path: `checkpoints/qm9_denoise.pth`. If readers want to train the diffusion model from the scratch, we suggest following the codes from [GDSS](https://github.com/harryjo97/GDSS). Our code should be compatible with any continuous-state graph diffusion model. For the graph diffusion model trained on other datasets, modifications for the `enbale_index` variable in the  `convert_sparse_to_dense `function from the `utils.mol_utils.py` are needed.


Following is an example command to run experiments on ABIDE datasets.

```
# ABIDE
python main.py --dataset ABIDE
```

The dataset name can be any of `['ABIDE', 'ADHD200','OSF']`

### Testing Process
We provide a checkpoint to facilitate the reproduction of the results. The checkpoint file is located in the path:

```
./BrainGS/checkpoints/ABIDE/best.pth.
```


