
# Research Topic:

## "Exploring Neurological Abnormality Detection in EEG Data with Provided Sleep Stage Annotations"

# Abstract:

This research aims to investigate the detection of neurological abnormalities in EEG data using a dataset containing EEG signals and provided sleep stage annotations. Leveraging comprehensive EEG recordings with accompanying sleep stage annotations, the study seeks to identify abnormal EEG patterns indicative of neurological dysfunction within the context of sleep stages. The primary objective is to develop a method for detecting abnormalities in EEG data that integrates sleep stage information to enhance the accuracy and interpretability of abnormality detection. Through rigorous experimentation and validation using real-world EEG datasets, the proposed approach aims to provide clinicians with a reliable tool for identifying potential neurological abnormalities based on EEG signals and sleep stage annotations. The findings of this research have the potential to contribute to advancements in neurological disorder diagnosis and treatment by providing a comprehensive understanding of abnormal EEG patterns within the context of sleep stages.


# Introduction:

Sleep is a vital physiological function that has a considerable impact on our emotional and physical well-being. A thorough examination of sleep habits can provide information about one's current state of health as well as potential warning signs for the future.
Understanding and treating a wide range of neurological and mental problems that can result from sleep disruptions require an understanding of sleep stages.Traditionally, EEG signals during sleep have been classified using the Rechtschaffen and Kales (R&K) guidelines. Stage 1, Stage 2, Stage 3, Stage 4, REM (Rapid Eye Movement), and movement time are the seven distinct stages that are specified by these principles. These phases, which correlate to various degrees of brain activity, are essential for preserving both physiological and cognitive processes. In order to improve the focus on important stages related to sleep disorders, recent updates to these criteria have reduced classification into three non-rapid eye movement (NREM) stages (N1, N2, N3) and one REM stage.        

These stages of sleep need to be clearly characterised because a variety of health issues are linked to irregular sleep patterns. On the other hand, irregularities in non-REM (rapid eye movement) sleep could indicate problems such as apnoea insensate, limb movement disorder, and even neurological conditions like Alzheimer's and Parkinson's. For example, mood disorders and cognitive decline have been associated with anomalies in rapid eye movement (REM) sleep. The intricacy of deciphering EEG data makes human classification labour-intensive and prone to error.    

![Introduction](Images/1.png)


# Plotting PSGs and Hypnograms 
![Introduction](Images/2(2).png)

![Introduction](Images/3(2).png)

# PSG Signals with sleep stages

![Introduction](Images/4.png)

# Feature Extraction Method

For this research paper we have used the EEMD method for extracting different features from the sleep dataset.EEMD, or Ensemble Empirical Mode Decomposition, is a technique used to decompose complex signals into simpler components. It’s an extension of the Empirical Mode Decomposition (EMD) method, which is particularly useful for analyzing non-linear and non-stationary time series data. 

# Dataset Description
We will utilize a comprehensive dataset comprising both cassette and sleep telemetry data. This dataset is specifically designed for the classification of sleep stages and includes recordings segmented into epochs, each representing a distinct sleep stage.

**Classification**
Our study focuses on two classification scenarios:

-**6-Class Classification:** Identifying and classifying each of the six different sleep stages.
-**5-Class Classification:** Aggregating certain sleep stages into a unified class to simplify classification.

# Data Preparation

**Segmentation:**

The sleep signals will be segmented into 30-second epochs. Each epoch will correspond to a single sleep stage, allowing for detailed analysis and classification of sleep stages.

-**Random Sampling:**
To address class imbalance, we will perform random sampling techniques to balance the dataset. This ensures that each sleep stage is represented equally in the training and evaluation phases, enhancing model performance.
Class Merging:

For the 5-class classification, specific sleep stages will be merged into a single class. This simplification aims to provide a more manageable classification problem and improve overall classification accuracy.

**Sleep Dataset:** https://www.physionet.org/content/sleep-edfx/1.0.0/#files-panel

## What is EEMD?
- **Empirical Mode Decomposition (EMD):** EMD decomposes a time series into Intrinsic Mode Functions (IMFs) and a residue. Each IMF represents a simple oscillatory mode of the data, and the residue is the trend component. While EMD is effective for analyzing time series data, it can be sensitive to noise and may result in mode mixing.

- **Ensemble Empirical Mode Decomposition (EEMD):**  EEMD addresses the limitations of EMD by introducing noise into the signal and performing EMD multiple times. The process involves:

- Adding white noise to the original signal.
- Decomposing the noisy signal into IMFs using EMD.
- Averaging the IMFs obtained from multiple realizations to get more stable and reliable results.

  



