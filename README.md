# DEFECT DETECTION IN CHEST X-RAY IMAGES

<img src="https://i.imgur.com/9amzklx.jpg" alt="Drawing" style="width: 650px;"/>


## PROJECT INTRODUCTION 

Thorax diseases are a major health threats on this planet. The pneumonia alone affects approximately 450 million people (i.e. 7% of the world population) and results in about 4 million deaths per year. Due to its low-cost and easy-access nature, chest radiography, colloquially called chest X-ray (CXR), is one of the most common types of radiology examinations for the diagnosis of thorax diseases.

The enormous number of chest radiographs produced globally are currently analyzed almost entirely through visual inspection on a slice-by-slice basis. This requires a high degree of skill and concentration, and is time-consuming, expensive, prone to operator bias, and unable to exploit the invaluable informatics contained in such large-scale data.

Moreover, due to the complexity of chest radiographs, it is challenging even for radiologists to discriminate thorax diseases on them, resulting in the shortage of expert radiologists who are competent to read chest radiographs in many countries. Therefore, there are significance demand to develop automated algorithms for the computer-aided diagnosis of thorax diseases on chest radiography.

## PROJECT GOAL

### 1. Frontal X-ray images preprocessing:
Pix2Pix was used to generate lung mask from full Chest X-ray image and OpenCV help to crop the image out.

<img src="https://i.imgur.com/fAMpwhD.png" alt="Drawing" style="width: 650px;"/>

### 2. Generate Labels for croped images:
The Croped-frontal image and lateral images then be processed by Model 1 and Model 2 to generate the result.

- Model 1: Classify images into 'No Finding' or 'Found' abnormalities in X-ray images.
- Model 2: Generate probabilities of multi-abnormalities labels for each X-ray image.

## DATASET

[Chest Xray Masks and Labels](https://www.kaggle.com/nikhilpandey360/chest-xray-masks-and-labels)
This dataset contains frontal chest X-ray images with lung masks which collected from the two datasets (Shenzhen and Montgomery) were published together in an analysis here: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4256233/.

[CheXpert - Stanford ML Group](https://stanfordmlgroup.github.io/competitions/chexpert/)
CheXpert is a large public dataset for chest radiograph interpretation, consisting of 224,316 chest radiographs of 65,240 patients. The chest radiographic examinations were retrospectively collected from Stanford Hospital, performed between October 2002 and July 2017 in both inpatient and outpatient centers, along with their associated radiology reports.

[MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/)
The MIMIC Chest X-ray (MIMIC-CXR) Database v2.0.0 is a large publicly available dataset of chest radiographs in DICOM format with free-text radiology reports. The dataset contains 377,110 images corresponding to 227,835 radiographic studies performed at the Beth Israel Deaconess Medical Center in Boston, MA.

# REFERENCES:

[CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning](https://arxiv.org/abs/1711.05225)

[Interpreting chest X-rays via CNNs that exploit hierarchical disease dependencies and uncertainty labels](https://arxiv.org/pdf/1911.06475.pdf)