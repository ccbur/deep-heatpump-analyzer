# deep-heatpump-analyzer
![Deep heat pump analyzer](/frost.jpg)
# To defrost or not to defrost - Using recurrent neural networks to predict defrosting events in an air/water heat pump

## Motivation

With this project I'm trying to predict defrosting events of my heat pump. The idea is to save some energy if I'm able to deactivate the heat pump shortly before a defrosting is happening.

## Warning

I implemented this project as part of the Udacity nanodegree in Datascience and should be considered preliminary. I'm still learning!

## Quick start
### Requirements
* Python >=3.5

### Packages
`pip install numpy pandas pytorch seaborn matplot calplot`

### Repository
`git clone https://github.com/ccbur/deep-heatpump-analyzer`

### Run

Open *analyze.ipynb* in your favorite Jupyter notebook application (Jupyter notebook, Visual Studio Code, Spyder, etc.). At least 8 GB of RAM is needed to run this notebook.

## Results
- The proposed pytorch model is using 5 features (hot_gas, probe_in, return, heatpump_running and defrosting) to predict if the heat pump will defrost in 5 minutes. It is based on a CNN with 10 filters, three LSTM layers and a linear classifier layer with two output classes (normal vs. defrosting).
    
    **>> The achieved weighted accuracy is 0.9948 and may be good enough to predict defrosting events 5 minutes before they happen.**

## Files
File | Description
------------ | -------------
*README.md* | this README
*analyze.ipynb* | Jupyter notebook to analyse the heat pump data and train the pytorch model
*data/xxx.csv.gz* | Raw data exported from my heat pump monitoring database
*gen/xxx.png* | Generated images

## License
The code is licensed under the [GNU General Public License v3.0](https://github.com/ccbur/deep-heatpump-analyzer/LICENSE).

## Acknowledgements
Thanks to Fei-Fei Li, Andrej Karpathy and Juston Johnson for the Stanford Winter Quarter 2016 class: CS231n: Convolutional Neural Networks for Visual (Youtube https://www.youtube.com/watch?v=NfnWJUyUJYU&list=PLkt2uSq6rBVctENoVBg1TpCC7OQi31AlC).
Thanks to hundreds of Blogs, Reddit users and Github project for their priceless infos on neural networks.
