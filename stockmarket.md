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

## Stock Market

<p align="justify">
The stock market is undoubtedly one of the most unpredictable, yet most popular areas for financial investment. Through facilitating exchanges of securities between buyers and sellers, this marketplace creates opportunities of capital gain for participants ranging from small individuals to big entities such as banks or conglomerates.

<p align="center"> 
  <img src="img/nse.png" alt="nyse" width=600>
  <br>Source from: <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nseindia.com%2F&psig=AOvVaw0LlyWlHOjM2IkaweHbaZqs&ust=1615225261667000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCJCIjJLdnu8CFQAAAAAdAAAAABAD">National Stock Exchange of Indea, Ltd.</a>
</p>
</p>

## Stock Market Price Change (Label)

<p align="justify">
	While there are countless financial measures in security discussions, this study focuses on one of the most direct assessments, i.e., the closing stock price. “The closing price is considered the most accurate valuation of a stock or other security until trading resumes on the next trading day” and is defined as “the last price at which the stock traded during the regular trading day” (Kenton). 

<br><br>As we purposefully structured this project as a classification task, this target for investigation is therefore transformed to be introduced as a binary label for model learning. For our project’s investigation purposes, we assign one class only to each day to represent trades that happen on that day. In specific, we compare the opening price to the closing price of a specific day in order to make a careful call on assigning an “increase” or “decrease” label to the combined daily stock entries.

<br><br>The India’s National Market Exchange market opens on 9:15 AM, and marks market closing on 3:30 PM across weekdays. We turned away from traditional considerations on pre-market hours and after-market hours for study, and adapted our target of investigation to be the price difference between the earliest opening price and latest closing price trading entries during a day. If this difference is of a positive output that signals an “increase” in stock value, while a negative output suggests the opposite. Therefore, summarizing that described above, given a particular day, we have our binary labels represented as the following:

</p>
<p align="center"> 
  <img src="img/pricelabel.png" alt="vol" width=250>
</p>

## NIFTY 100 Index Data
<p align = "justify">
	The stock index NIFTY 100 is specially chosen for this study. NIFTY 100 is a stock index in India’s National Stock Exchange and represents the major sectors of the country’s economy. This index is chosen after careful investigation into the condition of its available dataset. Compared to many other datasets on financial markets, NIFTY 100 stands out by its rather complete and integral structure.

    <p align="center"> 
  <img src="img/teslaback.jpg" alt="teslaback" width=500>
  <br>Source from: <a href="https://www.techfinanza.in/top-nifty-100-stocks/">Image Source</a>
</p>

<p>
Transaction data of NIFTY 100 from January 2, 2017 to January 1, 2021 were obtained. The following figure is a time series representation of the closing price of the data throughout this period. Here, one thing you can easily observe is that the trading has been especially volatile since the coronavirus pandemic in the early 2020. Although the stock price has been increasing throughout those past years, the extreme price drop at the beginning of the pandemic illustrates the uncertainty associated with stock trading and the exceptional difficulty to predict the price movements. <br><br>
	<p align="center"> 
	<b>Daily Closing Price of NIFTY 100 from 2017-01-02 to 2021-01-01</b><br>
  <img src="img/report_img/nifty100_3years_closing.png" alt="raw_data_close" width=600><br>
</p>

The focus of our prediction is to explore whether it’s possible to forecast if the index price increases or decreases thorough a day just by looking at the first one hour of trading. The below figure represents the closing price of NIFTY 100 on January 1, 2021. Here, we can observe that the index price ended up net-positive that day. However, inspecting closely, the price decreased during the first hours of trading that day and then the price later rose strongly. Again, this observation too indicates that our prediction task is very difficult for a human without much experience in the market to accurately perform. 
<p align="center"> 
	<b> Minute-level Closing Price of NIFTY 100 on 2021-01-01 - Full Market Hours</b><br>
  <img src="img/report_img/nifty100_20210101_closing.png" alt="20210101_full" width=600><br>
	<b>Minute-level Closing Price of NIFTY 100 on 2021-01-01 – First Market Hour.</b><br>
  <img src="img/report_img/nifty100_20210101_first_closing.png" alt="20210101_first" width=600><br>
</p>
This project's prediction task therefore builds upon this observation and the understanding that <i>the first hour of index price movement might be a helpful indicator for market behaviors of the day</i>. We then demonstrate this via research into modelling these stock prices with CNN recognition.
</p>