# Classification of PUBMED articles
**Text Mining Mid Project**\
Classified classes -> `cancer,virus,vaccine,COVID-19,genome`


### Index
* [Folder Structure](#folder-structure)
* [Order Project Execute](#order-project-execute)
* [Models Metrics Test](#models-metrics-test)
* [Final Model Metrics(SVM)](#final-model-metricssvm)

### Folder Structure

```
│──  Program
│       └── Classification.ipynb
│       └── Combine Datasets.ipynb
│       └── PUBMED txt_to_csv.ipynb
│──  Src
│       └──  All the PUBMED Arcticle int txt format
│       └──  ....
│──  Src_Parsed
│       └──  All the Parsed PUBMED article in CSV format
│       └──  One Combined Csv file with all the classes
│       └──  ....
│──  Trained Models
│       └── Trained Models Saves
│       └──  ....
│──  .gitignore
└──  README.md
```


### Order Project Execute
1. Create folders `Src`,`Src_Parsed` and `Trained Models` in the root directory (refer [Folder Structure](#folder-structure))
1. Download the PUBMED articles from website and save them in `Src` folder
1. Execute the `PUBMED txt_to_csv.ipynb` for each PUBMED article this saves a CSV file in `Src_Parsed` folder.
1. Execute the `Combine DataSets.ipynb`, this  will concatenate all the CSV files that are parsed in the previous execution i.e, `Src_Parsed` files into single file
1. Finally all our files are ready for the `Classification.ipynb`.


### Models Metrics Test

Params = `Lemmatization,TF-IDF(n_gram=1),5-Fold`

||Model|Accuracy|
|:-|:-|:-|
|❌|Naive Bayes|`0.9347882477438378`|
|❌|K-Nearest Neighbors|`0.8959708045067188`|
|❌|Decision tree|`0.9530726371235272`|
|❌|Random Forest|`0.9509715264106428`|
|✅|Support Vector Machine(SVM)|`0.9715043900251562`|


> _As the SVM model has the highest accuracy score among the other model we are using it for our final model_

### Final Model Metrics(SVM)

Params = `Lemmatization,TF-IDF(n_gram=1),30% Testing`


```python
=============== classification report ==================
              precision    recall  f1-score   support

      CANCER       0.99      0.99      0.99      2708
       COVID       0.97      0.96      0.96      2201
      GENOME       0.98      0.98      0.98      2631
     VACCINE       0.96      0.96      0.96      1921
       VIRUS       0.97      0.97      0.97      2166

    accuracy                           0.97     11627
   macro avg       0.97      0.97      0.97     11627
weighted avg       0.97      0.97      0.97     11627
=======================================================

F1 Score  = 0.9714981127994801
Recall    = 0.971460456171711
Precision = 0.9715500893609411
Accuracy  = 0.9727358733981251
```

