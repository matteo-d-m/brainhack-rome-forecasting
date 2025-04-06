# **I Know What You Will Do: Forecasting Motor Behaviour from EEG Time Series**

This repository contains code and supplementary information for Project #3 at [Brainhack Rome 2025](https://brainhackrome.github.io/). 

The official description of the project can be found at [this](https://github.com/brainhackrome/brainhackrome.github.io/issues/3) link.

The project leads are [Matteo De Matola](https://github.com/matteo-d-m) and [Anna Notaro](https://github.com/annanotaro).

## **The Big Picture**

This project aims at finding a deep learning solution to the problem of forecasting electroencephalography (EEG) time series.

Reliable EEG forecasting is required to predict the occurrence of pathological events (such as epileptic seizures) and to schedule stimulus delivery in an intelligent fashion, with applications to basic and clinical research. However, the multivariate and nonlinear nature of the EEG signal makes accurate forecasting hard to achieve ([De Matola & Miniussi, 2025](https://www.sciencedirect.com/science/article/pii/S1053811925000527)). Deep learning-based solutions might yield significant improvements to the state of the art, as suggested by two recent and pioneeering studies ([Pankka et al., 2024](https://www.biorxiv.org/content/10.1101/2024.01.16.575836v2.abstract), [Csaky et al., 2024](https://arxiv.org/abs/2404.09256)). Bulding on these studies, we will try to forecast EEG data acquired during a simple motor task, with potential applications to motor BCIs.

## Dataset

We will work on a version of the WAY-EEG-GAL dataset ([Luciw et al., 2014](https://www.nature.com/articles/sdata201447)), which contains multi-channel EEG signals recorded during thousands of grasp-and-lift trials. 

[Anna](https://github.com/annanotaro) and her colleagues at Bocconi University have optimised the dataset for use with machine learning. The entire dataset is quite heavy, so downloading it takes time. Moreover, your laptop is probably not powerful enough to run deep learning algorithms on it. Therefore, we have prepared a reduced version of the dataset, which we have stored on Google Drive at [this]() link. We have chosen Drive so you could mount the folder on [Google Colab](https://colab.research.google.com/) and avoid storing any data or running any program on your laptop.


## Set-up 

### Case 1 (easier): Remote Set-Up
Open file `eeg-forecasting-notebook.ipynb` from this repository and press the `Open in Colab` button. You will be sent to [Google Colab](https://colab.research.google.com/) (Google's free cloud computing platform), where your code can run on Google servers. 

Once in Colab, if you want your work to be saved to your Google Drive you must click on the `Copy to Drive` button, as shown below:

<p align="center">
  <img src="https://github.com/matteo-d-m/brainhack-rome-forecasting/blob/main/files/copy-to-drive.png" />
</p>

If you don't do so, your changes will get lost once you close the notebook.

### Case 2 (harder): Local Set-Up
If you:
1. Have a powerful laptop with a [CUDA-enabled GPU](https://en.wikipedia.org/wiki/CUDA) (you can check [here](https://developer.nvidia.com/cuda-gpus))
2. Have a functioning installation of the [CUDA toolkit](https://developer.nvidia.com/cuda-toolkit)
2. Have a [Miniconda or Anaconda](https://www.anaconda.com/docs/getting-started/getting-started) installation
3. Have a [git](https://git-scm.com/downloads) installation
4. Are used to working locally with Python and compute-intensive applications that run on a CUDA-enabled GPU

Then you can open a terminal, navigate to a directory of your choice and run: 

```
git clone https://github.com/matteo-d-m/brainhack-rome-forecasting.git
conda env create -f eeg-forecasting-env.yml
```