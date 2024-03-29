# Adaptive Real-Time Neural Decoder with Online Learning
This project experiments different learning methods for LSTM-based adaptive real-time neural decoder that predicts fine movements from neural activity signals extracted from animals' brains and continuously adapts to the data stream in an online setting. Compared to batch learning, We show that a combination of transfer learning that develops source model from other datasets and online learning that constantly updates the model to future data streams improves and better maintains model performance after deployment.

## Installation
Clone this repository by running ```git clone https://github.com/seungwonoh5/Online_Learning_Neural_Decoding```.

## Dependencies
To run our program, it requires the following:
* numpy==1.19.5
* pandas==1.1.5
* matplotlib==3.2.2
* tensorflow==2.4.1
* scikit-learn==0.22.2

All packages will automatically be installed after running ```pip3 install -r requirements.txt```.

## What's Included
Inside the repo, there are 4 scripts and 1 notebook file.
* data.py: this file provides all the data loading and preprocessing functions. (need to modify to use it for your own dataset)
* models.py: this file provides all the decoder models in Keras. 
* utils.py: this file provides all the visualization and misc functions.
* run.py: this file serves as the main script for the experiment that trains both the decoder and the baseline model and compare the results.
* main.ipynb: an example file that trains and plots the experimental results for visualization on Google Colab.

## Getting Started
You can either run the notebook ```main.ipynb``` which was run on Google Colab, or the main script(run.py) that imports other modules in the repo to go through the whole experiment. Individual modules in the neural decoding package can be reused at your needs.
```python run.py```

## Results
We perform extensive experiments on four datasets sequentially streaming and we show that an online setting continuously updating the model as every data block is processed leads to significant improvements over batch learning that the model is fixed after trained on an initial dataset and deployed for prediction. We show that performance of batch learning degrades after a few datasets where as online learning shows stable performance and even improves on future datasets.

![Alt text](result.png?raw=true "Title")

## Contact
Author: Seungwon Oh - [wonoh90@gmail.com](aspiringtechsavvy@gmail.com).
To ask questions or report issues, please open an issue on the issues tracker. Discussions, suggestions and questions are welcome!
