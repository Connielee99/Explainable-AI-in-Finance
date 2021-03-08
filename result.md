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

## Model Training Results

After the training procedure described above, the CNN model constantly achieves around **62% accuracy** on the validation set. The figure below shows the confusion matrix of our final model. We can observe that the model works quite equally for both of the two classes with the false positive rate being a little bit higher than the false negative rate.

<p align="center">
    <img src="img/report_img/confusion_matrix.png" alt="layers arch" width=400>
    <br>The Confusion Matrix of the Final Model

The figure below are some sample instances from the validation results. Again, the class “1” means the index price went up that given day and the class “0” indicates the opposite.
    
<p align="center">
    <img src="img/report_img/cnn_results.png" alt="layers arch" width=400>
    <br>Prediction Results for Some Instance in Validation Set