# Data Mining and Machine Learning
# Group 10

### Predicting Myocardial Infarction: A Comparative Analysis of Regression Models on Clinical Data and Image-Based Classification of ECG Patterns​

## Group Members
1. Archana Tharammal
2. Diab Rafeek
3. Furwa Asim
4. Harshitha Srikanth
5. Sana Sajesh

## Objective:
- Predict the likelihood of myocardial infarction (heart attack) by analyzing clinical data and ECG patterns.
- Compare the performance of regression models applied to clinical data.
- Implement and assess image-based classification models on ECG patterns to determine predictive capabilities based on visual cardiac signals.

## Key Milestones:
1. Milestone 1 (Week 3): Create hypothesis (R1)
    - Finalize the project title and research
    - Confirm the numerical and image datasets
    - Setup GitHub repository
    - Begin initial data exploration
2. Milestone 2 (Week 4): Data preprocessing (R2)
    - Dataset 1 preprocessing and cleaning
    - Draft tentative project plan
    - Create presentation for Project Pitch
    - Begin drafting of project report
    - Preprocessing of the ECG image dataset
3. Milestone 3 (Week 5-6): Implement clustering (R2 & R3)
    - Identify and select relevant features for modeling
    - Complete data analysis and exploration
    - Implement KMeans clustering
    - Evaluate clustering using various metrics
4. Milestone 4 (Week 7-8): Implement Regression models (R4)
    - Implement Decision trees and Random Forest
    - Implement Logistic Regression
    - Implement SVM and Naive Bayes
    - Train and evaluate the models
5. Milestone 5 (Week 9-10): Implement Neural Networks (R5)
    - Implement MLP for image classification
    - Implement CNN and compare with the models
    - Perform further data visualizations
6. Milestone 6 (Week 11-12): Finalized Documentation 
    - Summarize classification and regression results
    - Complete the final report as per requirements
    - Ensure code is well documented and uploaded to GitHub

## Datasets
1. Heart Statlog (Cleveland, Hungary) Dataset
    - **Source**: [Heart Statlog (Cleveland, Hungary)](https://www.kaggle.com/datasets/sid321axn/heart-statlog-cleveland-hungary-final)
    - **License**: This dataset is licensed under the [Creative Commons Zero (CC0) 1.0 Universal License](https://creativecommons.org/publicdomain/zero/1.0/)
    - ![Image](image.png)
2. ECG Images Dataset
    - **Source**: [ECG Images](https://www.kaggle.com/datasets/jayaprakashpondy/ecgimages)
    - ![Image](image-1.png)
      
## Data Preparation Pipeline 
1. Read the dataset file
2. Analyze the data

-- Patient dataset -- <br>
3. Remove null values<br>
4. Revove duplicates<br>
5. Handle outliers<br>

-- Image dataset -- <br>
3. Resize the images<br>
4. Convert to grayscale<br>
5. Normalize the data<br>
6. Flatten<br>
7. Perform data augmentation

#### How to run:
The Patient.ipynb file contains the code for patient dataset pre-processing, and the MLP.ipynb contains the code for image dataset preprocessing. Both these notebooks generate the new data into new folders as seen in the directory. These notebooks can be run with the original respective datasets to execute the pipeline 

## Requirements

#### R1: Project Topic, Direction, and Questions
- In this stage we finalised the project topic and the datasets.
- We also set up the Github Repository, began initial data exploration.

#### R2: Data Analysis and Exploration
- Conducted comprehensive data preprocessing and cleaning.
- Plotted diagrams like Histograms, box-plots, and bar charts for count.
- Used pearsons coefficient to identify correlation between features.
- [Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/Patient.ipynb)

#### R3: Clustering
- Implement KMeans using preprocessed data to identify patient groups with similar clinical characteristics 
- Evaluate clustering performance using metrics like the Elbow Method and Silhouette Analysis.
- Created a new dataset with clusters labeled, used for analysis later.
- [Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/KMeans.ipynb)

#### R4: Baseline Training and Evaluation Experiments
Apply at least three machine learning algorithms, such as:
- **Random Forest**: Implements decision trees for multiclass classification for data clustered by KMeans <br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/RandomForets.ipynb)
- **Logistic Regression**: Implements logistic regression for multiclass classification for data clustered by KMeans <br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/Logistic_Regression.ipynb)
- **SVM**: Implements SVM for binary MI classification <br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/Logistic_Regression.ipynb)
- **Naïve Bayes**: Implements Naive Bayes for multiclass classification for data clustered by KMeans<br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/Logistic_Regression.ipynb)


<table>
    <tr><td > </td>
        <td colspan="3"><b>Accuracy(%)</b></td>
        <td colspan="3", style="text-align:center;"><b> Precision </b></td>
        <td colspan="3", style="text-align:center;"><b> Recall </b></td>
        <td colspan="3", style="text-align:center;"><b> F1-Score </b></td></tr>
    <tr><td > </td>
        <th colspan="3"></th>
        <th>0</th><th>1</th><th>2</th>
        <th>0</th><th>1</th><th>2</th>
        <th>0</th><th>1</th><th>2</th></tr>
    <tr><td><b>Logistic Regression</b></td>
        <td colspan="3", style="text-align:center;">94.94</td>
        <td>0.95</td><td>0.93</td><td>0.98</td>
        <td>0.99</td><td>0.97</td><td>0.87</td>
        <td>0.97</td><td>0.95</td><td>0.92</td></tr>
    <tr><td><b>Random Forest</b></td>
        <td colspan="3", style="text-align:center;">92.70</td>
        <td>0.94</td><td>0.95</td><td>0.86</td>
        <td>0.96</td><td>0.94</td><td>0.83</td>
        <td>0.95</td><td>0.95</td><td>0.85</td></tr>
    <tr><td><b>Naïve Bayes</b></td>
        <td colspan="3", style="text-align:center;">93</td>
        <td>0.96</td><td>0.94</td><td>0.86</td>
        <td>0.94</td><td>0.92</td><td>0.91</td>
        <td>0.95</td><td>0.93</td><td>0.89</td></tr>
</table>


#### **R5: Neural Networks**
- Implement neural network models, such as:
    - **Multi-Layer Perceptrons (MLPs)**: Implements MLP for predictive analysis of patient class based on augmented ECG images <br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/MLP.ipynb)
    - **Convolutional Neural Networks (CNNs)**: Implements CNN to improve MLP results for predictive analysis of patient class based on augmented ECG images <br>
[Repo Location](https://github.com/harshis15/F21DLGroup10/blob/main/notebooks/CNN.ipynb)


<table>
    <tr>
        <td > </td>
        <td colspan="4"><b>Accuracy(%)</b></td>
        <td colspan="4", style="text-align:center;"><b> Precision </b></td>
        <td colspan="4", style="text-align:center;"><b> Recall </b></td>
        <td colspan="4", style="text-align:center;"><b> F1-Score </b></td>
    </tr>
    <tr><td > </td>
        <th colspan="4"></th>
        <th>Myocardial Infarction</th><th>Abnormal</th><th>History of MI</th><th>Normal</th>
        <th>Myocardial Infarction</th><th>Abnormal</th><th>History of MI</th><th>Normal</th>
        <th>Myocardial Infarction</th><th>Abnormal</th><th>History of MI</th><th>Normal</th></tr>
    <tr><td><b>MLP</b></td>
        <td colspan="4", style="text-align:center;">62.05</td>
        <td>0.67</td><td>0.65</td><td>0.56</td><td>0.61</td>
        <td>0.65</td><td>0.64</td><td>0.58</td><td>0.62</td>
        <td>0.66</td><td>0.64</td><td>0.57</td><td>0.61</td></tr>
    <tr><td><b>CNN</b></td>
        <td colspan="4", style="text-align:center;">84.48</td>
        <td>0.88</td><td>0.91</td><td>0.82</td><td>0.78</td>
        <td>0.85</td><td>0.90</td><td>0.71</td><td>0.91</td>
        <td>0.86</td><td>0.91</td><td>0.77</td><td>0.84</td></tr>
</table>

## File Structure on GitHub
- data/ <b><-- Contains the datasets --></b>
    - PatientData.zip 
    - heart_statlog_cleveland_hungary_final.csv 
    - updated_dataset_with_3_clusters.csv 
- documentation/ <b><-- Project docs and weekly updates --></b>
    - Summary of Algorithms/ <b><-- Individual summary of algorithms --></b> 
        - CNN.docx 
        - Clustering algorithms.docx 
        - Decision Trees.docx 
        - KMeans.docx 
        - LR.docx 
        - MLP.docx 
        - Naive Bayes.docx 
        - SVM.docx 
    - week3/ Week 3 summary.docx 
    - week4/
        - MYOCARDIAL INFARCTION A Global LIFE THREAT (1).pptx 
        - Week 4 summary.docx 
    - week5/ Week 5 summary.docx 
    - week6/ Week 6 summary.docx 
    - week7/ Week 7 summary.docx 
    - week8/ Week 8 summary.docx 
    - week9/ Week 9 summary.docx 
    - week10/ Week 10 summary.docx 
    - week11/ Week 11 summary.docx 
- notebooks/ <b><-- Jupyter notebook files for analysis and the models --></b>
    - models/
        - readme
            - mlp.keras 
    - models/ 
        - CNN.ipynb
        - KMeans.ipynb
        - Logistic_Regression.ipynb
        - MLP.ipynb
        - Naive Bayes (1).ipynb
        - Patient.ipynb
        - RandomForets.ipynb
        - RandomForets_unclustered.ipynb
        - SVM_Heart_Disease_Analysis.ipynb
        - Statistics for dataset.ipynb
        - requirements.txt
- README.md <b><-- README.md file --></b>
