# Machine learning for accessibility

Using machine learning to interpret the contents of nav elements in a site and predicting the aria-labels.

## Dataset

The dataset for this project is the `dataset.json` file and is already included in the project. It includes more than 1500 sites that are likely to be labeled for accessibility.

If you want to generate the dataset again or increase the amount of sites, do the following three steps.

* use `download_data.ipynb` to download some of the top sites in the `top-1m.csv` file.
* use `identify_useful_sites.ipynb` to check which ones are well labeled for accessibility.
* use `make_dataset.ipynb` to extract the data from the good sites and generating the `dataset.json` file

## Model

To train the model use the `model.ipynb` file. It is based on the translation pytorch tutorial [here](https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html). One small difference is that I removed the attention mechanisms to make things simpler. 

The results are just ok, but there are many ways to improve the model. One simple way could be to add the attention back. Another would be to pass other information about the nav elements directly to the decoder. And finally, increasing the dataset and training for a much longer time could also help.
