# Workshop 2: Medical image segmentation with CNNs - Tutorial

<a target="_blank" href="https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Part_1_abdominal_autoseg.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook 1 In Colab"/>
</a>

We will be using a suite of pre-built pytorch segmentation models in the excellent [segmentation-models](https://github.com/qubvel/segmentation_models.pytorch) package. This package simplifies the building of a pretrained segmentation network in 2D.

Pytorch can be quite intimidating, but is very powerful when you get to grips with it. In the interests of simplicity, we will use a wrapper around pytorch called [pytorch-lightning](https://pytorch-lightning.readthedocs.io/en/latest/). Lightning separates out the different bits of ML, allowing you to write a bit less boilerplate code, and letting us very quickly and easily use best-practise methods to train our models.
# Pre-requisites:
- Google account
- Basic knowledge of Python

# Part 1: Abdominal auto-segmentation

In Part 1, we will show you how to build an auto-segmentation model for abdominal organs-at-risk (OARs) using pytorch and pytorch-lightning. We will be using some open data from the [MICCAI 2021 FLARE Challenge](https://flare.grand-challenge.org/). This dataset contains ~500 patients, each of which has four OARs (liver, kidneys, pancreas and spleen) segmented. This notebook serves as an introduction and will walk you through the following steps:

1. Install prerequisites and set up
2. Load data containing CT and segmentations
3. Define some preprocessing and apply it to the CT slices
4. Create a segmentation model, using a library to make a pre-trained model for our segmentation task
5. Optimise a model on the training examples
6. Test the model against the testing data
7. Visualising the results! *(You'll need to do this yourself)*

**Important: As soon as you open a notebook, you should save your own copy to your Google Drive.** This will prevent people from editing the same notebook, which will lead to chaos...

To open this notebook in colab, click this link: [colab](https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Part_1_abdominal_autoseg.ipynb)

# Part 2: Head and neck auto-segmentation

In Part 2, we will move sites from the abdomen to the Head and Neck (HnN). We now want **you** to train a second CNN model to segment OARs at this site. The data for this section is originally from [The Cancer Imaging Archive (TCIA)](https://github.com/deepmind/tcia-ct-scan-dataset)

The notebook provided for this part has a skeleton code provided, you'll need to fill in the rest using what you learned from Part 1.
**Important: Remember to save your own copy as soon as you click the link below!**

To open the second notebook in colab, click this link: [colab](https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Part_2_head_and_neck_autoseg.ipynb)

# (Optional) Part 3: Image classification

In Part 3, you will train a CNN to classify head and neck CTs or abdominal CTs. You will then use the trained classifier to select the appropriate segmentation model (from Part 1 and Part 2) to segment random, unseen examples.

**Important: Remember to save your own copy as soon as you click the link below!**
To open in colab, click this link: [colab](https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Part_3_classifier.ipynb)
