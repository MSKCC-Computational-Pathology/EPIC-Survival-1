# EPIC-Survival 

This repository provides training and testing scripts for the article *EPIC-Survival: End-to-end Part Inferred Clustering for Survival Analysis with Prognostic Stratification Boosting* by **Muhammad and Xie et al. 2021**.

## How to Use
The main training script is `train.py`. Please use `python train.py --help` to see complete set of training parameters and their descriptions.

The tile library (csv) should have the following format:

SlideID | x | y | Duration | Event
------------ | ------------- | -------------| -------------| -------------
1 | 24521 | 23426 | 16.2 | 0 
1 | 6732 | 3323 | 16.2 | 0 
1 | 1232 | 5551 | 16.2 | 0
... | ... | ... | ... | ... 
324 | 34265 | 122 | 3.0 | 1 

The dataloader will load all `.svs` images at initiation, and pull tiles using the `(x,y)` coordinates during training.

## Python Dependencies
* torch 1.8.1
  * torchvision 0.9.1
* lifelines 0.23.8
* openslide 1.1.1
  * *Note: We recommend modifying openslide to correct for memory leak issue. Please see https://github.com/openslide/openslide-python/issues/24 for more information.*

## Reference
If you find our work useful, please consider citing our paper:

```bash
@inproceedings{muhammad2021epic,
  title={EPIC-Survival: End-to-end Part Inferred Clustering for Survival Analysis, with Prognostic Stratification Boosting},
  author={Muhammad, Hassan and Xie, Chensu and Sigel, Carlie S and Doukas, Michael and Alpert, Lindsay and Simpson, Amber Lea and Fuchs, Thomas J},
  booktitle={Medical Imaging with Deep Learning},
  year={2021}
}
```
