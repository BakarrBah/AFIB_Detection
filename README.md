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

PTB-XL data set is a large freely accessible clinical 12-Lead ECG waveform data, comprising of 21799 records from 18869 patients of 10 seconds long [2]. The data comprised of the raw signal data and a corresponding general metadata file. A detailed description of the data set and a source to the dataset is provided in the link below:

[^1]: *Wikipedia, "Electrocardiography," [Online]. Available: https://en.wikipedia.org/w/index.php?title=Electrocardiography&oldid=1132924386.*
