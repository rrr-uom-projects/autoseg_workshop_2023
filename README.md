# Workshop 2: Medical image segmentation with CNNs tutorial


<a target="_blank" href="https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Auto_segmentation_workshop.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook 1 In Colab"/>
</a>

# Part 1: Abdominal auto-segmentation

This notebook will show, briefly, how to build an autosegmentation model for abdominal organs-at-risk (OARs) using pytorch and pytorch-lightning. We will be using some open data from the [MICCAI 2021 FLARE Challenge](https://flare.grand-challenge.org/). This dataset contains ~500 patients, each of which has four OARs segmented.

We will be using a suite of pre-built pytorch segmentation models in the excellent [segmentation-models](https://github.com/qubvel/segmentation_models.pytorch) package. This package simplifies the building of a pretrained segmentation network in 2D. We will use a 2D approach, looping over slices in the data to segment 3D organs.

Pytorch can be quite intimidating, but is very powerful when you get to grips with it. In the interests of simplicity, we will use a wrapper around pytorch called [pytorch-lightning](https://pytorch-lightning.readthedocs.io/en/latest/). Lightning separates out the different bits of ML, allowing you to write a bit less boilerplate code, and letting us very quickly and easily use best-practise methods to train our models.


# Overview
The steps in this notebook make the following steps:

0. Install prerequisites and set up
1. Load data containing CT and segmentations
2. Define some preprocessing and apply it to the CT slices
3. Create a segmentation model, using a library to make a pre-trained model for our segmentation task
4. Train a the model to reproduce the training examples
5. Test the model against the testing data
6. Visualise the results!

# Running the first notebook
This notebook should be run on google colab, if you have access to that.

To open this notebook in colab, click this link: [colab](https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Auto_segmentation_workshop.ipynb)

# Part 2: Head and neck auto-segmentation

In part 2 we will move sites from the abdomen to the Head and Neck (HnN). We now want to train a second CNN model to segment OARs at this site. The data for this section is originally from [The Cancer Imaging Archive (TCIA)](https://github.com/deepmind/tcia-ct-scan-dataset)

The notebook provided for this part has a skeleton code provided, you'll need to fill in the rest using what you learned from part 1.

To open the second notebook in colab, click this link: [colab](https://colab.research.google.com/github/rrr-uom-projects/autoseg_workshop_2023/blob/main/Head_and_neck_notebook_2.ipynb)