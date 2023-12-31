# Variance-Aware Domain-Augmented Pseudo Labeling for Semi-Supervised Domain Generalization on Medical Image Segmentation
PyTorch implementation of Variance-Aware Domain-Augmented Pseudo Labeling for Semi-Supervised Domain Generalization on Medical Image Segmentation.

Huifeng Yao, Weihang Dai, Xiaowei Hu, Xiaowei Xu, Xiaomeng Li

<!-- Architecture:
- configs (config file)
- inference_mms.py(inference file for M&Ms dataset)
- inference_scgm.py(inference file for SCGM dataset)
- mms_dataloader.py(dataloader for M&Ms dataset)
- scgm_dataloader.py(dataloader for SCGM dataset)
- mms_train.py(train file for M&Ms dataset)
- scgm_train.py(train file for SCGM dataset) -->

## Preparation
### Datasets

* We followed the setting of [Semi-supervised Meta-learning with Disentanglement for Domain-generalised Medical Image Segmentation](https://arxiv.org/abs/2106.13292).
* We used two datasets in this paper: [Multi-Centre, Multi-Vendor & Multi-Disease Cardiac Image Segmentation Challenge (M&Ms) datast ](https://www.ub.edu/mnms/) and [Spinal cord grey matter segmentation challenge dataset](http://niftyweb.cs.ucl.ac.uk/challenge/index.php)
* We will release our CHD dataset soon. 
### Preprocessing

We followed the preprocessing of [Semi-supervised Meta-learning with Disentanglement for Domain-generalised Medical Image Segmentation](https://arxiv.org/abs/2106.13292), you can find the preprocessing code [here](https://github.com/xxxliu95/DGNet).
After that, you should change the data directories in the dataloader(mms_dataloader or scgm_dataloader) file.

### Environments
We use [wandb](https://wandb.ai/site) to visulize our results. If you want to use this, you may need register an account first.

Use this command to install the environments.
```
conda env create -f VDPL_environment.yaml
```
## How to Run

### Training
If you want to train the model on M&Ms dataset, you can use this command. You can find the config information in config/mms.yaml.
```
bash mms_run.sh
```

### Evaluate
If you want to evaluate our models on M&Ms dataset, you can use this command. And you should change the model name(line 320 and 321) and the test_vendor(line 318) to load different models.
```
python inference_mms.py
```


## Main Results

## Citation
