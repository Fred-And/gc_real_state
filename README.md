<h1 align="center">Real State Price Prediction</h1>
<h3 align="center">A linear regression problem.</h3>

<p align="center">
  We all know that <strong> planning is the core of any successful business </strong>. Concerned about dealing with a high demand of new Real State for sale, the CEO of a Real State Company asked for a predictive algorithm that based on the historical data provided by him, could estimate the price of a real state.
<br>
<br>
The first thing I did, was to check the data provided by the company and all the variables. After importing it to my notebook, I found out that I was dealing with <strong>5000 rows by 4 Columns dataset</strong> and the variables were the following:
  <ul>
    <li> Price
    <li> Area
    <li> Distance from the beach
    <li> Distance from the drugstore
  </ul>  
<br>
The CEO asked for a price prediction so, since the beginning, I knew that <strong>my dependent variable was the Price</strong>, the next step was to find the best independent variables to explain the phenomena. Before starting, I quickly checked the frequency distribution of the Real State prices and saw something like this:
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/histogram.png'>
<br>
From this moment I knew I'd have to transform the data, probably by using log.
<br>
I had three possible variables, so, to understand better the behavior of each one, I decided to do a PairPlot using the Seaborn Python library. The results were the following.
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/pairplot01.png'>
<br>
It was not that hard to see that the <strong>Price and the Real State Area were strongly correlated</strong>, the distance from the beach was also relevant but not as much as the area. The distance from the drugstore got me to question its relevance for the model, <strong>but I'm a data scientist, not a data guesser, so let's keep it and eliminate it only if the stats tell me so.</strong>
<br>
<br>
Before modeling, I transformed the data using the Log Transformation aiming to achieve a normal distribution of the price and it happened.
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/histogram_normal.png'>
<br>

Now that we have the log of the price, area, and distances, let's see the correlation again!
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/pairplot02.png'>
<br>

<h3>Great! let's go tho the modeling.</h3>
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/summary.png'>
<br>
Using "statsmodels.summary()" to have a panorama of my model, I scientifically got to conclusion that the distance from the drugstore indeed wasn't relevant for my model, let's cut it out.
<br>
Now my independent variables look something like this:
<ul>
  <li> Area
  <li> Distance from the beach
</ul>
<br>
After testing the model, I got this point:
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/pred_real.png'>
<br>
A few residuals but I think that's still acceptable, what about we check the residuals distribution?
<br>
<img src='https://github.com/Fred-And/linear_regression/blob/main/img/residuals.png'>
<br>
To be honest...way better than I expected!
<br>
More information about the code and what I did to get to all those conclusions, in the notebook!  
</p>

<h3 align="left">Connect with me on LinkedIn:</h3>
<p align="left">
<a href="https://linkedin.com/in/https://www.linkedin.com/in/fredericocandrade/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/fredericocandrade/" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools used in this project:</h3>
<p align="left"> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> </p>
