# ARC



## Dependency

The environment of our codes can be found in ``requirement.txt``.

## ARC Calculation

ARC (Average Relative Confusion) is a new unsupervised evaluation metric for contrastive learning proposed in this paper, which estimates the degree of ''chaos'' of augmented samples by calculating the ratio of samples whose nearest neighbour is from the same anchor. We find that it's strongly correlated to the downstream performance of contrastive learning process. We think that it may be helpful in model selection and some other tasks to improve the performance of contrastive learning.

To calculate ACR and ARC with trained models, run ``evaluate_ARC.py`` with following commands

```
./ARC_test.sh
```

The code for ACR and ARC calculation can be found in ``ARC.py``.

## ACR results

We observe the relation between ARC and downstream performance of SimCLR with RandomResizedCrop of different augmentation strength in the following figure

![image](https://user-images.githubusercontent.com/81618067/156936579-a2f2ae6e-0cea-4da5-9444-8e6ba6a5a64e.png)



## GARC Calculation

To avoid the outliers, we propose a generalized version of ACR as GACR. Correspondingly, ARC is extended to GARC.

To calculate GACR and GARC with trained models, run ``evaluate_AGRC.py`` with following commands

```
./GARC_test.sh
```

The code for GACR and GARC calculation can be found in ``ARC.py``.


## Synthetic results

The code of the synthetic dataset can be found in ``synthetic_data.ipynb``.


## Acknowledgement

This baseline of this repo mainly borrows from [SimCLR](https://github.com/AndrewAtanov/simclr-pytorch).
