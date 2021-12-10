# Amplification of labeled data for feature type inference using active learning
## Abstract
AutoML is the process that allows the automation of applying ML to real world problems, accelerating ML research and enabling non-ML experts to participate in deployment of ML models. Our focus lies on the task of data preparation for ML on structured data, primarily aimed on the step of ML feature type inference. This is a vital step in ensuring optimal performance of downstream ML models, as poor feature type inference can significantly degrade the model’s performance. Labeled data is a rare and very valuable commodity, and we explore the amplification of labeled datasets using active learning. SortingHat is an ML-based method to perform feature type inference on real world data; it is more accurate than other existing methods that employ rule-based heuristics. We integrateSortingHat into an active learning pipeline to learn the impact of using a human-in-the-loop approach to improve SortingHat’s feature type inference on the benchmarked dataset; we observe an increase in accuracy from 92.65% to 93.5%. We also aim to contribute to the augmenting of the benchmarked dataset.


## Running the code
Our final experiments are available in [active_learning.ipynb](https://github.com/eiffelwong1/feature-type-inference-using-AL/blob/main/colab_notebooks/active_learning.ipynb). The notebook should be run sequentially from the first cell to the last cell.

Note: Older undocumented versions of our work can be found in `colab_notebooks/older_versions`. Code for utility functions can be found in `colab_notebooks/utility`.

## Dependencies
The entire dependency list from the virtual environment used for our experiments can be found in the [requirements.txt](https://github.com/eiffelwong1/feature-type-inference-using-AL/blob/main/requirements.txt) file. We use Python version `3.8.6` for our experiments.

### Members
- Rahul Patil (MS CSE Student, UCSD)
- Sing Wong (MS CSE Student, UCSD)
