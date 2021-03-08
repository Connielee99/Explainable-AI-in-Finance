## Navigation 
- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance">HomePage</a>
- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/abstract">Project Details</a>
  - <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/introduction">Introduction</a>
  - <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/stockmarket">Stock Market</a>
  - <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/result">Prediction Result</a>
- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/methodology">Technical Methodology</a>
	- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/gaf">Gramian Angular Field</a> 
	- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/fastai">FastAI CNN Model</a>
	- <a href = "https://connielee99.github.io/Explainable-AI-in-Finance/gradcam">Grad-CAM Algorithm</a>


## Market Prediction with CNN Model using FastAI Library 

 
We used **FastAI**, a PyTorch-based deep learning library, to build the neural network. This enables us to figure out the relationship between input features and find hidden relationships within them. The input data is an image dataset with labels -- converted from time series with Gramian Angular Field as described in the previous section.


The entire dataset of 988 days (image instances) was divided into training and validation sets, with a 20% validation ratio. Our training procedure followed the following steps.
 

1.	Create a baseline model, i.e., ResNet-34.<br>
2.	Find the optimal learning rate for the initial layers where the numerical gradients are minimized.<br>
3.	Train the model with the learning rate found in (1) with 10 epochs.<br>
4.	Unfreeze the model and find the optimal learning rate for all the layers where the numerical gradients are minimized.<br>
5.	Train the model with the learning rate found in (3) with 10 epochs.<br>

 
For the CNN network, the pretrained **ResNET-34** is utilized as the bottom layers. We added [1024, 2] dense layers on top and a simple linear activation node for the final regression as a custom head (See Table 1). Table 1 below shows the architecture of the top layers of the model. For the loss function, our final model utilizes Cross-Entropy loss, and for model performance measuring metric, we leverage the use of accuracy scores.
 


<p align="center">
    <img src="img/report_img/cnn_top_layers.png" alt="layers arch" width=400>
    <br>Top Layers Summary on CNN Learner
