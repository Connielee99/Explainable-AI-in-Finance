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
<p align="center"> 
	<b>Grad-CAM Architecture</b><br>
  <img src="img/gradcamalg.png" alt="gradcamalg">
  <br>Published by: <a href="https://arxiv.org/abs/1610.02391">Ramprasaath R. Selvaraju, et.al.,</a>
</p>

| Predicted Class = 1 | GAF Image: 2017-01-03 | GAF Image: 2021-01-01 |
| --- | --- | --- |
| Original Image | <img src="img/test_imgs/2017-01-03.png" alt="test1" width=250> | <img src="img/test_imgs/2021-01-01.png" alt="test2" width=250> |
| Grad-CAM | <img src="img/class1_layer4_2017-01-03/0-resnet34-gradcam-layer4-oscilloscope.png" alt="test11" width=250> | <img src="img/class1_layer4_2021-01-01/0-resnet34-gradcam-layer4-digital_clock.png" alt="test21" width=250> |
| Vanilla Backpropagation | <img src="img/class1_layer4_2017-01-03/0-resnet34-vanilla-oscilloscope.png" alt="test12" width=250> | <img src="img/class1_layer4_2021-01-01/0-resnet34-vanilla-digital_clock.png" alt="test22" width=250> |
| DeconvNet | <img src="img/class1_layer4_2017-01-03/0-resnet34-deconvnet-oscilloscope.png" alt="test13" width=250> | <img src="img/class1_layer4_2021-01-01/0-resnet34-deconvnet-digital_clock.png" alt="test23" width=250> |
| Guided Backpropagation | <img src="img/class1_layer4_2017-01-03/0-resnet34-guided-oscilloscope.png" alt="test14" width=250> | <img src="img/class1_layer4_2021-01-01/0-resnet34-guided-digital_clock.png" alt="test24" width=250> |
| Guided Grad-CAM | <img src="img/class1_layer4_2017-01-03/0-resnet34-guided_gradcam-layer4-oscilloscope.png" alt="test15" width=250> | <img src="img/class1_layer4_2021-01-01/0-resnet34-guided_gradcam-layer4-digital_clock.png" alt="test25" width=250> |
