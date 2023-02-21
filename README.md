# Project Title

Model accuracy analysis in emotion recognition dataset

## Description

This is an overall emotion recognition model evlauation, mainly using 
`
tensorflow.keras
`
and `train-test split` in
`
scikit-learn
`
to get both
1. Overall model score using `classification_report`, `confusion_matrix` from `scikit-learn`
2. Model score in individual emotion dataset

## Getting Started

### Emotion recognition dataset 

The dataset used in this analysis reprot is from [FER - 2013 dataset with 7 emotion types](https://www.kaggle.com/datasets/ananthu017/emotion-detection-fer) that contained 35,000+ images for training and testing. The emotion categories are (with demos):
* angry
  * ![image](https://user-images.githubusercontent.com/47016159/220430758-900be79e-acb9-4536-ac04-66766b940521.png)
* disgusted
  * ![image](https://user-images.githubusercontent.com/47016159/220430907-bdc54fac-b448-42e9-ab31-db6f8124a81c.png)
* fearful
  * ![image](https://user-images.githubusercontent.com/47016159/220431019-c83d7738-8b41-4b7a-aeb1-d608ba687a6c.png)  
* happy
  * ![image](https://user-images.githubusercontent.com/47016159/220431119-7842ada1-4b6a-4a0d-ac24-d574d4391481.png) 
* neutral
  * ![image](https://user-images.githubusercontent.com/47016159/220431217-5932350a-541d-44c3-a39e-9d7b3cbded2a.png)
* sad
  * ![image](https://user-images.githubusercontent.com/47016159/220431299-1e13cccd-ef7a-4a07-9aaa-60860da5559f.png) 
* surpried
  * ![image](https://user-images.githubusercontent.com/47016159/220431510-e5e7acbe-1b5b-49ff-bc0c-04411ef0adbc.png)

### Overall model score

Confusion matrix:
<br>
![image](https://user-images.githubusercontent.com/47016159/220433202-66a3e3b4-74f4-4eef-ab19-7b975b3e9cd4.png)
![image](https://user-images.githubusercontent.com/47016159/220431788-a7616013-db2f-4feb-b6cc-1a72be630168.png)

The overall evaluation of the whole dataset yields an confusion matrix. In here, it's when we need to investigate 
**True Positive**, **True Negative**, **False Positive**, and **False Negative**. 
There are also four scoring metrcis:
* Accuracy
* Precision
* Recall
* F-1 Score

In this case, they all have a range of 62%-63%, which is very consistent. But overall, I prefer to make F-1 score as the standard accuracy value to deal with the 
imbalance dataset.

### Individual emotion dataset accuracy

I renamed each image name in each emotion category folder. The image ended up with a numerical value so I can loop through the folder to allow model to inference. After all,
the accuracy value for each emotion is:
* angry: 41.78%
* disgust: 31.82%
* fearful: 39.42%
* happy: 85.23%
* neutral: 2.85%
* sad: 17.58%
* surprised: 5.56%

### Conclusion

The accuracy we have above showed that the emtion recognition model is decent at the very least, meaning it's enoguh for the company's business purpose even if we were seeking a model with the accuracy of 75% - 80%. 
One issue needs to be aware of is lacking diversity of human race in this dataset. For example, this dataset does not have enough of Asain faces, and this might cause issues or wrong
emotion detection in a more boradly use. 

## Contact

[Shih-Hsi Chien (LinkedIn)](https://www.linkedin.com/in/shih-hsi-chien/)
<br>
shihhsi.chien@gmail.com

## Sources
* [Kaggle emotion dataset](https://www.kaggle.com/datasets/ananthu017/emotion-detection-fer)
