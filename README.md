# Amplification of labeled data for feature type inference using active learning
## Abstract
AutoML is the process that allows the automation of applying ML to real world problems, accelerating ML research and enabling non-ML experts to participate in deployment of ML models. Our focus lies on the task of data preparation for ML on structured data, primarily aimed on the step of ML feature type inference. This is a vital step in ensuring optimal performance of downstream ML models, as poor feature type inference can significantly degrade the model’s performance. Labeled data is a rare and very valuable commodity, and we explore the amplification of labeled datasets using active learning. SortingHat is an ML-based method to perform feature type inference on real world data; it is more accurate than other existing methods that employ rule-based heuristics. We integrateSortingHat into an active learning pipeline to learn the impact of using a human-in-the-loop approach to improve SortingHat’s feature type inference on the benchmarked dataset; we observe an increase in accuracy from 92.65% to 93.5%. We also aim to contribute to the augmenting of the benchmarked dataset.


## Running the code
Our final experiments are available in [active_learning.ipynb](https://github.com/eiffelwong1/feature-type-inference-using-AL/blob/main/colab_notebooks/active_learning.ipynb). The notebook should be run sequentially from the first cell to the last cell.

Note: Older undocumented versions of our work can be found in `colab_notebooks/older_versions`. Code for utility functions can be found in `colab_notebooks/utility`.

## Dependencies
The entire dependency list from the virtual environment used for our experiments can be found in the [requirements.txt](https://github.com/eiffelwong1/feature-type-inference-using-AL/blob/main/requirements.txt) file. We use Python version `3.8.6` for our experiments.

## File Structure
.
├── README.md
├── RulebookForLabeling.pdf 
├── active_learning.ipynb       # main active learning notebook
├── active_learning_alt.ipynb   # notebook with some additional graph plotting
├── older_versions              # older version of the notebooks
├── requirements.txt
└── utility
    ├── data_split_234.ipynb    # notebook for creating stratified training and simulation data split
    └── plotter.ipynb           # contains some graph plotting function

## Benchmark
The benchmark dataset for the feature type inference problem is obtained from SortingHat's [ML-Data-Prep-Zoo](https://github.com/pvn25/ML-Data-Prep-Zoo/tree/master/MLFeatureTypeInference). For further details about the project, visit: [SortingHat](https://adalabucsd.github.io/sortinghat.html)

## Results
|                    Approaches                   |     9-class   Accuracy    |         |      Numeric     |               |         |     Categorical    |               |         |      Datetime    |               |         |      Sentence    |               |         |        URL       |               |         |     Embedded   Number    |               |         |        List      |               |         |     Not-Generalizable    |               |         |     Context-Specific    |               |         |
|:-----------------------------------------------:|:-------------------------:|:-------:|:----------------:|:-------------:|:-------:|:------------------:|:-------------:|:-------:|:----------------:|:-------------:|:-------:|:----------------:|:-------------:|:-------:|:----------------:|:-------------:|:-------:|:------------------------:|:-------------:|:-------:|:----------------:|:-------------:|:-------:|:------------------------:|:-------------:|:-------:|:-----------------------:|:-------------:|:-------:|
|                                                 |                           |         |     Precision    |     Recall    |         |      Precision     |     Recall    |         |     Precision    |     Recall    |         |     Precision    |     Recall    |         |     Precision    |     Recall    |         |         Precision        |     Recall    |         |     Precision    |     Recall    |         |         Precision        |     Recall    |         |         Precision       |     Recall    |         |
|        [Random   Forest (Shah et al. 2021)](https://adalabucsd.github.io/papers/TR_2021_SortingHat.pdf)       |           0.9265          |         |       0.936      |      0.987    |         |         0.91       |      0.954    |         |       0.986      |      0.972    |         |       0.899      |      0.87     |         |         1        |      0.969    |         |           0.919          |      0.919    |         |       0.956      |      0.754    |         |           0.946          |      0.888    |         |           0.852         |      0.714    |         |
|             Active Learning (Ranked batch-mode sampling=20)            |           0.931          |         |       0.947      |      0.987    |         |        0.921       |      0.957    |         |       0.986      |      0.986    |         |       0.862      |      0.881    |         |       1      |      0.969    |         |           0.939          |      0.929    |         |         0.977        |      0.754    |         |           0.927          |      0.896    |         |           0.864         |      0.737    |         |
|       Active Learning (Ranked batch-mode sampling=40)            |           0.935          |         |       0.951      |      0.989    |         |        0.930       |      0.954    |         |       0.986      |      0.986    |         |       0.863      |      0.891    |         |       1      |      0.969    |         |           0.929          |      0.929    |         |         0.977        |      0.771    |         |           0.939          |      0.913    |         |           0.854         |      0.745    |         |
Active Learning (Ranked batch-mode sampling=60)            |           0.934          |         |       0.951      |      0.987    |         |        0.922       |      0.957    |         |       0.986      |      0.986    |         |       0.864      |      0.902    |         |       1      |      0.936    |         |           0.939          |      0.929    |         |         0.977        |      0.754    |         |           0.939          |      0.913    |         |           0.854         |      0.737    |         |
| Active Learning (Ranked batch-mode sampling=80)            |           0.931          |         |       0.947      |      0.987    |         |        0.922       |      0.952    |         |       0.986      |      0.979    |         |       0.863      |      0.891    |         |       1      |      0.969    |         |           0.939          |      0.929    |         |         0.977        |      0.754    |         |           0.936          |      0.901    |         |           0.849         |      0.741    |         |

### Members
- Rahul Patil (MS CSE Student, UCSD)
- Sing Wong (MS CSE Student, UCSD)
