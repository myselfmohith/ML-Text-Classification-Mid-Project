<!-- Source Links -->

# Project Report

|Model Parameters||
|:-|:-|
|TOkenization|Lemmatisation|
|Feature Extraction|`(1,1) Gram`|
|Feature Weighting|TF-IDF|
|Training Test|K-Fold|

The above parameters are the base parameters for comparison of the models.


### Tokenization
|Model|Lemmatisation|Stemming|
|:-|:-|:-|
|Naive Bayes|`0.9347882477438378`||
|K-Nearest Neighbors|`0.8959708045067188`||
|Decision tree|`0.9530726371235272`||
|Random Forest|`0.9509715264106428`||
|Support Vector Machine(SVM)|`0.9715043900251562`||

### Feature Extraction
Comaprision of `1-gram vs 2-gram vs 1-2-gram`

#### 1-Gram (1,1)
|Model|1-Gram|2-Gram|1x2-Gram|
|:-|:-|:-|:-|
Naive Bayes|`0.9347882477438378`|||
K-Nearest Neighbors|`0.8959708045067188`|||
Decision tree|`0.9530726371235272`|||
Random Forest|`0.9509715264106428`|||
Support Vector Machine(SVM)|`0.9715043900251562`|||

### Feature Weighting

|Model|TF-IDF|BOW|
|:-|:-|:-|
|Naive Bayes|`0.9347882477438378`||
|K-Nearest Neighbors|`0.8959708045067188`||
|Decision tree|`0.9530726371235272`||
|Random Forest|`0.9509715264106428`||
|Support Vector Machine(SVM)|`0.9715043900251562`||


### Training Test

|Model|K-Fold (K=5)|30% Test 70% Train|
|:-|:-|:-|
|Naive Bayes|`0.9347882477438378`||
|K-Nearest Neighbors|`0.8959708045067188`||
|Decision tree|`0.9530726371235272`||
|Random Forest|`0.9509715264106428`||
|Support Vector Machine(SVM)|`0.9715043900251562`||


### Final CLassifier Metrics

|Metric|Value|
|:-|:-|
|Tokenization||
|Feature Extraction||
|Feature Weighting||
|Classifier||
|Training time||
|Testing Time||
|Accuracy||
|Presicion||
|Recall||
|F1 Score||