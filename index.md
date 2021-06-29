---
title: Little data is often enough for distance-based outlier detection
---

We show that using only a small fraction of the data to train distance-based outlier detection models often leads to no significant reduction in predictive performance over a wide range of datasets.

This page contains additional information not included in the published paper. If you would like to refer to our work, please cite our work as follows:

```
@article{Muhr2022,
  doi = {TBD},
  url = {TBD},
  year = {2022},
  publisher = {TBD},
  volume = {TBD},
  number = {TBD},
  pages = {TBD},
  author = {David Muhr and Michael Affenzeller},
  title = {Little data is often enough for distance-based outlier detection},
  journal = {TBD}
}
```

The datasets used in our study stem from Campos et al.'s review on the evaluation of unsupervised outlier detection and comprise a range of tabular datasets, see [DAMI datasets](https://www.dbs.ifi.lmu.de/research/outlier-evaluation/DAMI/). Additionally, we use twelve proprietary datasets consisting of high-dimensional manufacturing sensor data. See the table below for an overview.

| Dataset                               | Description                                                             | N      | Outliers | Dim   |
|---------------------------------------|-------------------------------------------------------------------------|--------|----------|-------|
| Datasets used in the literature       |                                                                         |        |          |       |
| [ALOI](#aloi)                         | Images represented with histograms features                             | 50,000 | 1508     | 27    |
| [Glass](#glass)                       | A dataset describing types of glass using class 6 as outlier            | 214    | 9        | 7     |
| [Ionosphere](#ionosphere)             | Differentiates bad radars for structures in the Ionosphere              | 351    | 126      | 32    |
| [KDDCup99](#kddcup99)                 | Data describing network intrusions or attacks                           | 60,632 | 246      | 41    |
| [PenDigits](#pendigits)               | Hand-written digits with class 4 downsampled as outliers                | 9,868  | 20       | 16    |
| [Shuttle](#shuttle)                   | Space shuttle data using class 2 as outliers                            | 1,013  | 13       | 9     |
| [Waveform](#waveform)                 | Three classes of waves and with class 0 downsampled as outliers         | 3,443  | 100      | 21    |
| [WBC](#wbc)                           | Benign or malignant cancer types with malignant as outliers             | 454    | 10       | 9     |
| [WDBC](#wdbc)                         | Nuclear characteristics for breast cancer with malignant outliers       | 367    | 10       | 30    |
| Semantically meaningful datasets      |                                                                         |        |          |       |
| [Annthyroid](#annthyroid)             | Hypothyroidism data with classes other than normal as outliers          | 7,200  | 534      | 21    |
| [Arrhythmia](#arrhythmia)             | Cardiac arrhythmia patient records with arrhythmia as outliers          | 450    | 206      | 259   |
| [Cardiotocography](#cardiotocography) | Data set related to heart diseases with other than normal as outliers   | 2,126  | 471      | 21    |
| [HeartDisease](#heartdisease)         | Medical data on heart problems with affected patients are outliers      | 270    | 120      | 13    |
| [InternetAds](#internetads)           | Web images classified as ads or not with ads being outliers             | 3,264  | 454      | 1,555 |
| [PageBlocks](#pageblocks)             | Different types of blocks in document pages with non-text as outliers   | 5,473  | 560      | 10    |
| [Pima](#pima)                         | Patients suffering from diabetes are considered outliers                | 768    | 268      | 8     |
| [SpamBase](#spambase)                 | Data set representing emails classified as normal or spam (outliers)    | 4,601  | 1,813    | 57    |
| [Stamps](#stamps)                     | Differentiate geniune (ink) stamps from forged stamps (outliers)        | 340    | 31       | 9     |
| [Wilt](#wilt)                         | Differentiates diseased trees (outliers) from other land covers         | 4,839  | 261      | 5     |
| Proprietary datasets                  |                                                                         |        |          |       |
| [Sensor1a](#sensor1a)                 | Detect different defects (outliers) using sensor point 1 on machine 'a' | 1,000  | 30       | 3001  |
| [Sensor1b](#sensor1b)                 | Detect different defects (outliers) using sensor point 1 on machine 'b' | 1,000  | 30       | 3001  |
| [Sensor1c](#sensor1c)                 | Detect different defects (outliers) using sensor point 1 on machine 'c' | 1,000  | 30       | 3001  |
| [Sensor2a](#sensor2a)                 | Detect different defects (outliers) using sensor point 2 on machine 'a' | 1,000  | 30       | 3001  |
| [Sensor2b](#sensor2b)                 | Detect different defects (outliers) using sensor point 2 on machine 'b' | 1,000  | 30       | 3001  |
| [Sensor2c](#sensor2c)                 | Detect different defects (outliers) using sensor point 2 on machine 'c' | 1,000  | 30       | 3001  |
| [Sensor3a](#sensor3a)                 | Detect different defects (outliers) using sensor point 3 on machine 'a' | 1,000  | 30       | 1440  |
| [Sensor3b](#sensor3b)                 | Detect different defects (outliers) using sensor point 3 on machine 'b' | 1,000  | 30       | 1440  |
| [Sensor3c](#sensor3c)                 | Detect different defects (outliers) using sensor point 3 on machine 'c' | 1,000  | 30       | 1440  |
| [Sensor4a](#sensor4a)                 | Detect different defects (outliers) using sensor point 4 on machine 'a' | 1,000  | 30       | 1440  |
| [Sensor4b](#sensor4b)                 | Detect different defects (outliers) using sensor point 4 on machine 'b' | 1,000  | 30       | 1440  |
| [Sensor4c](#sensor4c)                 | Detect different defects (outliers) using sensor point 4 on machine 'c' | 1,000  | 30       | 1440  |

For each dataset, we provide a plot showing the best ROC AUC result for a specific sampling/prototype fraction with the corresponding best value of k. You can see the individual results for each dataset below.

In case there are any questions, please contact the author at firstname.lastname@bmw.com.

### Datasets used in the literature

#### ALOI

##### KNN

![](results/literature/KNN-ALOI_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-ALOI_withoutdupl_norm.png)

#### Glass

##### KNN

![](results/literature/KNN-Glass_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-Glass_withoutdupl_norm.png)


#### KDDCup99

##### KNN

![](results/literature/KNN-KDDCup99_withoutdupl_norm_idf.png)

##### LOF

![](results/literature/LOF-KDDCup99_withoutdupl_norm_idf.png)

#### PenDigits

##### KNN

![](results/literature/KNN-PenDigits_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-PenDigits_withoutdupl_norm.png)

#### Shuttle

##### KNN

![](results/literature/KNN-Shuttle_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-Shuttle_withoutdupl_norm.png)

#### Waveform

##### KNN

![](results/literature/KNN-Waveform_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-Waveform_withoutdupl_norm.png)

#### WBC

##### KNN

![](results/literature/KNN-WBC_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-WBC_withoutdupl_norm.png)

#### WDBC

##### KNN

![](results/literature/KNN-WDBC_withoutdupl_norm.png)

##### LOF

![](results/literature/LOF-WDBC_withoutdupl_norm.png)

### Semantically meaningful datasets

#### Annthyroid

##### KNN

![](results/semantic/KNN-Annthyroid_withoutdupl_norm_02.png)
![](results/semantic/KNN-Annthyroid_withoutdupl_norm_05.png)
![](results/semantic/KNN-Annthyroid_withoutdupl_norm_07.png)

##### LOF

![](results/semantic/LOF-Annthyroid_withoutdupl_norm_02.png)
![](results/semantic/LOF-Annthyroid_withoutdupl_norm_05.png)
![](results/semantic/LOF-Annthyroid_withoutdupl_norm_07.png)

#### Arrhythmia

##### KNN

![](results/semantic/KNN-Arrhythmia_withoutdupl_norm_02.png)
![](results/semantic/KNN-Arrhythmia_withoutdupl_norm_05.png)
![](results/semantic/KNN-Arrhythmia_withoutdupl_norm_10.png)
![](results/semantic/KNN-Arrhythmia_withoutdupl_norm_20.png)
![](results/semantic/KNN-Arrhythmia_withoutdupl_norm_46.png)

##### LOF

![](results/semantic/LOF-Arrhythmia_withoutdupl_norm_02.png)
![](results/semantic/LOF-Arrhythmia_withoutdupl_norm_05.png)
![](results/semantic/LOF-Arrhythmia_withoutdupl_norm_10.png)
![](results/semantic/LOF-Arrhythmia_withoutdupl_norm_20.png)
![](results/semantic/LOF-Arrhythmia_withoutdupl_norm_46.png)

#### HeartDisease

##### KNN

![](results/semantic/KNN-HeartDisease_withoutdupl_norm_02.png)
![](results/semantic/KNN-HeartDisease_withoutdupl_norm_05.png)
![](results/semantic/KNN-HeartDisease_withoutdupl_norm_10.png)
![](results/semantic/KNN-HeartDisease_withoutdupl_norm_20.png)
![](results/semantic/KNN-HeartDisease_withoutdupl_norm_44.png)

##### LOF

![](results/semantic/LOF-HeartDisease_withoutdupl_norm_02.png)
![](results/semantic/LOF-HeartDisease_withoutdupl_norm_05.png)
![](results/semantic/LOF-HeartDisease_withoutdupl_norm_10.png)
![](results/semantic/LOF-HeartDisease_withoutdupl_norm_20.png)
![](results/semantic/LOF-HeartDisease_withoutdupl_norm_44.png)


#### InternetAds

##### KNN

![](results/semantic/KNN-InternetAds_withoutdupl_norm_05.png)
![](results/semantic/KNN-InternetAds_withoutdupl_norm_10.png)
![](results/semantic/KNN-InternetAds_withoutdupl_norm_19.png)

##### LOF

![](results/semantic/LOF-InternetAds_withoutdupl_norm_05.png)
![](results/semantic/LOF-InternetAds_withoutdupl_norm_10.png)
![](results/semantic/LOF-InternetAds_withoutdupl_norm_19.png)

#### PageBlocks

##### KNN

![](results/semantic/KNN-PageBlocks_withoutdupl_norm_02.png)
![](results/semantic/KNN-PageBlocks_withoutdupl_norm_05.png)
![](results/semantic/KNN-PageBlocks_withoutdupl_norm_09.png)

##### LOF

![](results/semantic/LOF-PageBlocks_withoutdupl_norm_02.png)
![](results/semantic/LOF-PageBlocks_withoutdupl_norm_05.png)
![](results/semantic/LOF-PageBlocks_withoutdupl_norm_09.png)

#### Pima

##### KNN

![](results/semantic/KNN-Pima_withoutdupl_norm_02.png)
![](results/semantic/KNN-Pima_withoutdupl_norm_05.png)
![](results/semantic/KNN-Pima_withoutdupl_norm_10.png)
![](results/semantic/KNN-Pima_withoutdupl_norm_20.png)
![](results/semantic/KNN-Pima_withoutdupl_norm_35.png)

##### LOF

![](results/semantic/LOF-Pima_withoutdupl_norm_02.png)
![](results/semantic/LOF-Pima_withoutdupl_norm_05.png)
![](results/semantic/LOF-Pima_withoutdupl_norm_10.png)
![](results/semantic/LOF-Pima_withoutdupl_norm_20.png)
![](results/semantic/LOF-Pima_withoutdupl_norm_35.png)

#### SpamBase

##### KNN

![](results/semantic/KNN-SpamBase_withoutdupl_norm_02.png)
![](results/semantic/KNN-SpamBase_withoutdupl_norm_05.png)
![](results/semantic/KNN-SpamBase_withoutdupl_norm_10.png)
![](results/semantic/KNN-SpamBase_withoutdupl_norm_20.png)
![](results/semantic/KNN-SpamBase_withoutdupl_norm_40.png)

##### LOF

![](results/semantic/LOF-SpamBase_withoutdupl_norm_02.png)
![](results/semantic/LOF-SpamBase_withoutdupl_norm_05.png)
![](results/semantic/LOF-SpamBase_withoutdupl_norm_10.png)
![](results/semantic/LOF-SpamBase_withoutdupl_norm_20.png)
![](results/semantic/LOF-SpamBase_withoutdupl_norm_40.png)

#### Stamps

##### KNN

![](results/semantic/KNN-Stamps_withoutdupl_norm_02.png)
![](results/semantic/KNN-Stamps_withoutdupl_norm_05.png)
![](results/semantic/KNN-Stamps_withoutdupl_norm_09.png)

##### LOF

![](results/semantic/LOF-Stamps_withoutdupl_norm_02.png)
![](results/semantic/LOF-Stamps_withoutdupl_norm_05.png)
![](results/semantic/LOF-Stamps_withoutdupl_norm_09.png)

#### Wilt

##### KNN

![](results/semantic/KNN-Wilt_withoutdupl_norm_02.png)
![](results/semantic/KNN-Wilt_withoutdupl_norm_05.png)

##### LOF

![](results/semantic/LOF-Wilt_withoutdupl_norm_02.png)
![](results/semantic/LOF-Wilt_withoutdupl_norm_05.png)

### Proprietary datasets

#### Sensor1a

##### KNN

![](results/proprietary/KNN-Sensor1a.png)

##### LOF

![](results/proprietary/LOF-Sensor1a.png)

#### Sensor1b

##### KNN

![](results/proprietary/KNN-Sensor1b.png)

##### LOF

![](results/proprietary/LOF-Sensor1b.png)

#### Sensor1c

##### KNN

![](results/proprietary/KNN-Sensor1c.png)

##### LOF

![](results/proprietary/LOF-Sensor1c.png)

#### Sensor2a

##### KNN

![](results/proprietary/KNN-Sensor2a.png)

##### LOF

![](results/proprietary/LOF-Sensor2a.png)

#### Sensor2b

##### KNN

![](results/proprietary/KNN-Sensor2b.png)

##### LOF

![](results/proprietary/LOF-Sensor2b.png)

#### Sensor2c

##### KNN

![](results/proprietary/KNN-Sensor2c.png)

##### LOF

![](results/proprietary/LOF-Sensor2c.png)


#### Sensor3a

##### KNN

![](results/proprietary/KNN-Sensor3a.png)

##### LOF

![](results/proprietary/LOF-Sensor3a.png)

#### Sensor3b

##### KNN

![](results/proprietary/KNN-Sensor3b.png)

##### LOF

![](results/proprietary/LOF-Sensor3b.png)

#### Sensor3c

##### KNN

![](results/proprietary/KNN-Sensor3c.png)

##### LOF

![](results/proprietary/LOF-Sensor3c.png)

#### Sensor4a

##### KNN

![](results/proprietary/KNN-Sensor4a.png)

##### LOF

![](results/proprietary/LOF-Sensor4a.png)

#### Sensor4b

##### KNN

![](results/proprietary/KNN-Sensor4b.png)

##### LOF

![](results/proprietary/LOF-Sensor4b.png)

#### Sensor4c

##### KNN

![](results/proprietary/KNN-Sensor4c.png)

##### LOF

![](results/proprietary/LOF-Sensor4c.png)
