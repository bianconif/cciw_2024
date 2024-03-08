# Classification of lung nodules on CT via pseudo-colour images and deep features from pre-trained convolutional networks

### by [Francesco Bianconi](www.bianconif.net), Mario Luca Fravolini, Elena Caltana, [Muhammad Usama Khan](https://www.linkedin.com/in/usama-khan-0a509211a/) and Barbara Palumbo

### Submitted to the [Computational Color Imaging Workshop (CCIW 2024)](http://www.ivl.disco.unimib.it/minisites/cciw-2024/index.html)

## Supplementary material

### Features
- LIDC-IDRI (multi-volume zip archive): part [1](data/LIDC-IDRI.zip.001), [2](data/LIDC-IDRI.zip.002), [3](data/LIDC-IDRI.zip.003), [4](data/LIDC-IDRI.zip.004) and [5](data/LIDC-IDRI.zip.005)
- [LUNGx](data/LUNGx.zip)

##### Key to fields
- Features are denoted by name (where conventional features) or number (deep features) preceded by the prefix `Feature____`
- `PrimaryKey` denotes the unique lung nodule id
- `Malignancy` denotes the target class (`N` for benign and `P` for malignant)
- The other fields dentote dataset-dependent metadata

#### File naming convention
- `hc` indicates conventional (hand-crafted) radiomics features
- `gs`, `pca` or `pcl` indicates the pseudo-colouring method – respectively denoted as GS, PCA and PCL in the paper
- `convnext`, `resnet50` and `swin_v2` indicates the pre-trained CNN – respectively ConvNeXT, ResNet50 and Swin V2
- `avgpool` indicates the layer of the CNN model used for feature extraction
- `br` or `f` respectively denotes whether background removal was used or not

### Complete results
- [`results-complete.csv`](data/results-complete.csv)

##### Key to fields
- `Train`, `Test`: train and test dataset
- `Feature`: the feature set (follows the file naming convention – see above)
- `Classifier`, `Scaler` the classifier and the feature scaling method used (see Sec. 3.3 of the paper)
- `Eval-mode`: the accuracy evaluation method (`4-fold` for internal validation and `full` for cross validation)
- `Accuracy`, `Sensitivity` and `Specificity`: the figures of merit  

### Folds (for internal validation)
- ['folds-LIDC-IDRI.csv'](data/folds-LIDC-IDRI.csv)
- ['folds-LUNGx.csv'](data/folds-LUNGx.csv)
