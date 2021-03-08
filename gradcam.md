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

## Gradient-Weighted Class Activation Map

<p align='justify'>
	Grad-CAM is an “Explainable AI” technique developed in 2016 by Selvaraju et al. It is introduced with a primary goal of boosting confidence in applying neural networks – making it possible for visual analysis on misclassified instances for detecting discrepancies. By “producing ‘visual explanations’ for decisions from large class of CNN-based models, making them more transparent”, Grad-CAM helps people better understand a wide range of tasks, including image classification, image captioning, and visual question answering models, etc. (Selvaraju et al.).

Briefly summarizing the working process of Grad-CAM (see Figure below): given a picture and a class as input, Grad-CAM forward-propagates the image through the network model to get raw class scores before the Softmax layer (Selvaraju et al.). A gradient signal with only the inputted class set to 1 and others to 0 is then back-propagated to the rectified Conv feature maps – where coarse localization is calculated and a heatmap is generated (Selvaraju et al.). Finally, the pointwise multiplications of this heatmap and guided backpropagation produces Guided Grad-CAM visualizations (Selvaraju et al.).<br>

<p align="center"> 
	<b>Grad-CAM Architecture</b><br>
  <img src="img/gradcamalg.png" alt="gradcamalg">
  <br>Published by: <a href="https://arxiv.org/abs/1610.02391">Ramprasaath R. Selvaraju, et.al.,</a>
</p>


