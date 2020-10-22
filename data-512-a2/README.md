# Human Centered Data Science - A2: Bias in Data 

The goal of this assignment is to identify potential sources of bias may exist in the Perspective API datasets, and to develop testable hypotheses about how these biases might impact the behavior of machine learning models trained on the data, when those models are used for research purposes or to power data-driven applications. 

## API Documentation

This project will use two datasets from the Wikipedia Talk corpus, which has open access to public through the [Perspective API](https://github.com/conversationai/perspectiveapi/blob/master/2-api/methods.md). Each dataset contains thousands of online discussion posts made by Wikipedia editors who were discussing how to write and edit Wikipedia articles. 

Dataset description and schemas: https://meta.wikimedia.org/wiki/Research:Detox/Data_Release

The following two datasets are used in this project:

1. Toxicity Dataset: [Documentation](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Toxicity) [Download](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973)

2. Personal Attacks Dataset: [Documentation](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Personal_Attacks) [Download](https://figshare.com/articles/Wikipedia_Talk_Labels_Personal_Attacks/4054689)

## Analysis

1. Analyze the demographic information about the Crowdflower workers that is available in the Toxicity and Personal Attacks dataset.
2. Analyze and compare the demographic biases in the two datasets.
3. Explore relationships between worker's gender and labeling behavior in the two datasets.

## Packages
- pandas
- numpy
- matplotlib

## License

This code is available under the [MIT License](LICENSE)