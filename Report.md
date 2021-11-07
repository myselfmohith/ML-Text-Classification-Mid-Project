# Project Report

Team Members
* Arige Tejasri
* Bhavanam Vijaya Durga
* Mederametla TarunTeja
* Mohith Kumar Bezawada


| Model Parameters   |                |
| :----------------- | :------------- |
| TOkenization       | Lemmatisation  |
| Feature Extraction | `(1,1) Gram`   |
| Feature Weighting  | TF-IDF         |
| Training Test      | K-Fold `(K=5)` |

The above parameters are the base parameters for comparison of the models. We will be updating the parameters on each step with best fit

### Tokenization

| Model                       | Lemmatisation ✅     | Stemming             |
| :-------------------------- | :------------------- | :------------------- |
| Naive Bayes                 | `0.9347882477438378` | `0.9329453374348800` |
| K-Nearest Neighbors         | `0.8959708045067188` | `0.9007632613750800` |
| Decision tree               | `0.9530726371235272` | `0.9515241752884643` |
| Random Forest               | `0.9509715264106428` | `0.948390582296198`  |
| Support Vector Machine(SVM) | `0.9715043900251562` | `0.9710989280151379` |

### Feature Extraction

Comaprision of `1-gram vs 2-gram vs 1-2-gram`

| Model                       | Uni-Gram `(1,1)` ✅  | Bi-Gram `(2,2)`      | Uni and Bi-Gram `(1,2)` |
| :-------------------------- | :------------------- | :------------------- | :---------------------- |
| Naive Bayes                 | `0.9347882477438378` | `0.9437830823089375` | `0.9463633198068354`    |
| K-Nearest Neighbors         | `0.8959708045067188` | `0.3275178836834426` | `0.9020532102642846`    |
| Decision tree               | `0.9530726371235272` | `0.9441274462997641` | `0.9527039599402773`    |
| Random Forest               | `0.9509715264106428` | `0.9509872448385228` | `0.9421612478576439`    |
| Support Vector Machine(SVM) | `0.9715043900251562` | `0.9702335876108725` | `0.9707257036864661`    |

### Feature Weighting

| Model                       | TF-IDF ✅            | BOW                  |
| :-------------------------- | :------------------- | :------------------- |
| Naive Bayes                 | `0.9347882477438378` | `0.9534410153536225` |
| K-Nearest Neighbors         | `0.8959708045067188` | `0.700704190949533`  |
| Decision tree               | `0.9530726371235272` | `0.9525564265585906` |
| Random Forest               | `0.9509715264106428` | `0.9517087245061753` |
| Support Vector Machine(SVM) | `0.9715043900251562` | `0.9710989280610872` |

### Training Test

| Model                       | K-Fold (K=5)         | 30% Test 70% Train ✅ |
| :-------------------------- | :------------------- | :-------------------- |
| Naive Bayes                 | `0.9347882477438378` | `0.9372151027780167`  |
| K-Nearest Neighbors         | `0.8959708045067188` | `0.892491614345919`   |
| Decision tree               | `0.9530726371235272` | `0.9540724176485766`  |
| Random Forest               | `0.9509715264106428` | `0.9560505719446116`  |
| Support Vector Machine(SVM) | `0.9715043900251562` | `0.9730799002322181`  |

### Final CLassifier Metrics

| Metric             | Value                |
| :----------------- | :------------------- |
| Tokenization       | Lemmatisation        |
| Feature Extraction | Uni Gram `(1,1)`     |
| Feature Weighting  | TF-IDF               |
| Classifier         | SVM                  |
| Training time      | 3min 4s              |
| Testing Time       | 1min 25s             |
| Accuracy           | `0.9730799002322181` |
| Precision          | `0.9702119000775948` |
| Recall             | `0.9698185269508628` |
| F1 Score           | `0.9699648491304906` |

Here is the complete classification report from `sklearn` library using the best model parametres(SVM).

```python
              precision    recall  f1-score   support

      CANCER       0.98      0.99      0.99      2670
       COVID       0.97      0.96      0.96      2206
      GENOME       0.98      0.98      0.98      2683
     VACCINE       0.96      0.96      0.96      1880
       VIRUS       0.97      0.97      0.97      2188

    accuracy                           0.97     11627
   macro avg       0.97      0.97      0.97     11627
weighted avg       0.97      0.97      0.97     11627

F1 Score  = 0.9699648491304906
Recall    = 0.9698185269508628
Precision = 0.9702119000775948
Accuracy  = 0.971101745936183
```
