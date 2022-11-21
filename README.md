# MalFamilyClassifier
The source code for the paper "[Imbalanced Malware Family Classification Using Multimodal Fusion and Weight Self-learning](https://ieeexplore.ieee.org/abstract/document/9913918)".

## Scripts

The scripts of MalFamilyClassifier are divided into three parts:

- Feature engineering
  - features.ipynb : Feature extraction classes of multimodal (the byte, format, statistic, and semantic, etc.) features.
  - feature_engineering.ipynb : Feature vectorization & feature-based multimodal fusion of extracted features.
- Model construction
  - model.ipynb : Base model class for training, cross-validation and predicting.
  - train.ipynb : The training function based on the features and model.
  - predict.ipynb : Predicting functions for different strategies of model construction.
- Others
  - experiment.ipynb : Comparison experiments to validate MalFamilyClassifier.
  - utils.ipynb : Helpful functions using in other scripts.

## Data

The directory of all types of data is organized as follows:

```
|-- /                             # "data_path" defined in the scripts
    |-- raw_data                  # dataset (after pre-processing on original opensource datasets)
        |-- train # training set
            |-- pe                # samples in PE format
            |-- asm               # samples in ASM format
        |-- train                 # test set
            |-- pe
            |-- asm
    |-- user_data                 # temporary data generated during the running process
        |-- feature               # feature vocabularies, feature vectors, weight matrix, etc.
        |-- models                # pre-trained models, feature selectors, trained models, etc.
        |-- semantic              # semantic files corresponding to samples in the dataset.
        |-- other temprory files
    |-- prediction_result         # results predicted by models and metrics
```

## Links

- [2021 CCF BDCI Digital Security Open on "Malware family classification based on Artificial Intelligence"](https://www.datafountain.cn/competitions/507) **Rank 2/724**
  - [Code](https://gitee.com/LizhengyangSec/malware_-classification_-bdci/tree/master) | [Writeup](https://mp.weixin.qq.com/s/q0ScSZyXFK8XLgMTBU9k5g)

## Citation
If you use the scripts for your research please cite the following paper:

 ```
S. Li, Y. Li, X. Wu, S. A. Otaibi and Z. Tian, "Imbalanced Malware Family Classification Using Multimodal Fusion and Weight Self-Learning," in IEEE Transactions on Intelligent Transportation Systems, 2022, doi: 10.1109/TITS.2022.3208891.
 ```
 
 ```bib
@ARTICLE{9913918,  author={Li, Shudong and Li, Yuan and Wu, Xiaobo and Otaibi, Sattam Al and Tian, Zhihong},  journal={IEEE Transactions on Intelligent Transportation Systems},   title={Imbalanced Malware Family Classification Using Multimodal Fusion and Weight Self-Learning},   year={2022},  volume={},  number={},  pages={1-11},  doi={10.1109/TITS.2022.3208891}}
```
