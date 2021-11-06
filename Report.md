<!-- Source Links -->

# Project Report

|Model Parametres||
|:-|:-|
|TOkenization|Lemmatisation|
|Feature Extraction|`(1,1) Gram`|
|Feature Weighting|TF-IDF|
|Training Test|K-Fold|

The above parametres are the base parametres for comparisition of the models.

### Feature Extraction - 3
Comaprision of `1-gram vs 2-gram vs 1-2-gram`

#### 1-Gram (1,1)
||Model|Accuracy|
|:-|:-|:-|
|❌|Naive Bayes|`0.9347882477438378`|
|❌|K-Nearest Neighbors|`0.8959708045067188`|
|❌|Decision tree|`0.9530726371235272`|
|❌|Random Forest|`0.9509715264106428`|
|✅|Support Vector Machine(SVM)|`0.9715043900251562`|

#### 2-Gram (2,2)

#### 1x2-Gram (1,2)

### Feature Weighting - 2
Comaprision of `TF-IDF vs BOW`

#### TF-IDF
||Model|Accuracy|
|:-|:-|:-|
|❌|Naive Bayes|`0.9347882477438378`|
|❌|K-Nearest Neighbors|`0.8959708045067188`|
|❌|Decision tree|`0.9530726371235272`|
|❌|Random Forest|`0.9509715264106428`|
|✅|Support Vector Machine(SVM)|`0.9715043900251562`|

#### BOW

### Training Test - 2

#### K-Fold(K=5)
||Model|Accuracy|
|:-|:-|:-|
|❌|Naive Bayes|`0.9347882477438378`|
|❌|K-Nearest Neighbors|`0.8959708045067188`|
|❌|Decision tree|`0.9530726371235272`|
|❌|Random Forest|`0.9509715264106428`|
|✅|Support Vector Machine(SVM)|`0.9715043900251562`|

#### 30% Test 70% Train