# **ATRIAL FIBRILATION**

---

## 1.0 BACKGROUND

Hearth arrhythmia is an irregular heartbeat and occurs when the electrical signals that regulate heartbeat do not function properly. This irregularity may cause the heart to beat too fast (tachycardia), too slow (bradycardia) or irregular. In general, Arrhythmias are categorized by rate, mechanism and/or duration.
Atrial fibrillation (A-fib) is the most common type of arrhythmia and affects more than 33 million people worldwide. A-fib increases the risk of stroke, heart failure and other heart-related complications. A-fib may cause a fast, pounding heartbeat, shortness of breath or weakness. A-fib is a serious medical condition that requires proper treatment to prevent stroke.

Early detection is important to reduce the risks of A-fib related complications. Electrocardiography (ECG) provides a key non-invasive diagnostic tool for assessing the cardiac clinical status of a patient. This project is to build a machine learning model to detect A-fib on patients using ECG data.

## 1.1 Electrocardiography (ECG)

ECG is the process of recording the heart’s electrical activity. The ECG is a graph of the voltage versus time of the heart electrical activity using electrodes place on the skin[^1]. In a 12-lead ECG, ten electrodes are placed on the patient’s limbs and on the surface of the chest. This configuration allows for the magnitude of the heart electric potential to be measured from twelve different angles (leads). Teh figure below shows an illustration of the relevant components of the conduction system, the heart, and the classical ECG Waveforms.

![ECG IMAGE](/images/ECG2X.png)

## 2.0 DATA

PTB-XL data set is a large freely accessible clinical 12-Lead ECG waveform data, comprising of 21799 records from 18869 patients of 10 seconds long[^2]. The data comprised of the raw signal data and a corresponding general metadata file. A detailed description of the data set and a source to the dataset is provided in the link below:

[PTB-XL Description and Source](https://physionet.org/content/ptb-xl/1.0.3/)

## 3.0 METHOD

Several machine learning (ML) models for ECG analysis have been successfully implemented. Most of these models used traditional ml algorithms and signal processing techniques. Traditional ML models require some prior domain knowledge and expertise to define relevant features. For example, features like the P-wave, QRS Complex and T wave may be required to be used as inputs to the model. Thus, feature engineering is an important step to transform the raw data in to the relevant feature representation[^3]. To eliminate the need for domain knowledge feature extraction a deep learning model, in particular 1D-CNN (Convolutional Neural Network), is used on this project. A 1D-CNN, Kernel slides along one dimension. A 1D-CNN is an appropriate tool for the ECG analysis as the date is two dimensional and moves along the time axis.

## 4.0 DATA WRANGLING

[DATA WRANGLING](/01_DataWrangling.ipynb)

The PTB-XL database, which contains the metadata of all ECG records was imported from the local drive (The dataset was downloaded and save locally from [here](https://physionet.org/content/ptb-xl/1.0.3/)). The final cleaned data set was saved as a new file for future use. The cleaned database was then used to load the ECG data with a sampling rate of 100 Hz.
![Missing Data Figure](/images/missing_data.png)

## 5.0 EXPLORATORY DATA ANALYSIS

The figure below shows a plot of the heart rhythm Vs. number of ECG records. The data is imbalanced and may impact the result of the model. Consideration should be given to rebalance the data.

![Heart Rythm](/images/ECG_HeartRhythm.png)

The figure below shows a plot of the number of the Arrhythmia with age. The data shows that younger people tend to have normal heart rhythm but they are also likely to have other arrhythmias. However, older people tend to be more likely to be diagnosed with AFIB. This suggests that adding age to the model may help improve the accuracy of the model.

![Age Heart Rythm](/images/ECG_Age.png)

[^1]: *Wikipedia, "Electrocardiography," [Online]. Available: https://en.wikipedia.org/w/index.php?title=Electrocardiography&oldid=1132924386.*

[^2]: *P. Wagner, N. Strodthoff, R.-D. Bousseljot, D. Kreiseler, F. I. Lunze, W. Samek and T. Schaeffter, "PTB-XL, a large publicly available electrocardiography dataset," Nature, [Online]. Available: https://doi.org/10.1038/s41597-020-0495-6.*

[^3]: *A. Peimankar and S. Puthusserypady, "DENS-ECG-A deep learning approach for ECG signal delineation," ELSEVIER, vol. 165, 2021*

