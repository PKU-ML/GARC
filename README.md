# GARC



## Dependency

The environment of our codes can be found in ``requirement.txt``.

## ARC Calculation

ARC (Average Relative Confusion) is a new unsupervised evaluation metric for contrastive learning proposed in this paper, which estimates the degree of ''chaos'' of augmented samples by calculating the ratio of samples whose nearest neighbour is from the same anchor. We find that it's strongly correlated to the downstream performance of contrastive learning process. We think that it may be helpful in model selection and some other tasks to improve the performance of contrastive learning.

To calculate ACR and ARC with trained models, run ``evaluate_ARC.py`` with following commands

```
./ARC_test.sh
```

The code for ACR and ARC calculation can be found in ``ARC.py``.

## GARC Calculation

To avoid the outliers, we propose a generalized version of ACR as GACR. Correspondingly, ARC is extended to GARC.

To calculate GACR and GARC with trained models, run ``evaluate_GARC.py`` with the following commands

```
./GARC_test.sh
```

The code for GACR and GARC calculation can be found in ``ARC.py``.


## Synthetic Dataset Experiments

The code of experiments on the synthetic dataset to verify the influence of the augmentation strength can be found in ``synthetic_data.ipynb``.

## Visualization of Augmentation Graph

The augmentation graph of CIFAR-10 with different strength r of RandomResizedCrop can be visualized with the following commands. 

```
python connect_cifar.py
```


## Acknowledgement

This baseline of this repo mainly borrows from [SimCLR](https://github.com/AndrewAtanov/simclr-pytorch).
