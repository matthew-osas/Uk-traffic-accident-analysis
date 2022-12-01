![MasterHead](https://www.arabnews.com/sites/default/files/styles/n_670_395/public/2018/11/11/1365101-921132596.gif?itok=8bwmmW9h)
<h1 align="center">Hi 👋, I'm Matthew Osadebamwen</h1>
<h3 align="center">A passionate I.T Support Desk Analyst and Data Scientist with crazy interest in Artificial Intelligence</h3> 
<img align="right" alt="Coding" width="400" src="https://cdn.dribbble.com/users/207059/screenshots/16573416/media/4f24405796465a71b2691f94f5e5d1f8.gif"

<p align="left"> <img src="https://komarev.com/ghpvc/?username=matthew-osas&label=Profile%20views&color=0e75b6&style=flat" alt="matthew-osas" /> </p>

- 🔭 I’m currently working on **Analysing Road Traffic Accidents in the UK for the year 2019**

- 🌱 I’m currently learning **Linux**

- 📫 How to reach me **osadebamwen.matthew@gmail.com**

- ⚡ Fun fact **I think I'm good at Chess even though I barely win any game nowadays.**

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://linkedin.com/in/matthew-osadebamwen-ba4b26110" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="matthew-osadebamwen-ba4b26110" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://cloud.google.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"> <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://opencv.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://pytorch.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="pytorch" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> </p>



# UK Traffic Aaccident Aanalysis
For this analysis we will use the road safety data available from here: http://data.gov.uk/dataset/road-accidents-safety-data

## <font color = red>**Introduction**</font>
The UK government provides detailed road safety data with respect to injuries, road accidents, type of vehicles involved and casualties. Overall, the data is divided into three datasets: Accidents, Vehicles and Casualties. A summary of each of these datasets is presented in Table 1. The ‘accident index’ is provided in each dataset to identify an accident. I initially proposed to merge all three datasets from the start, before performing the analysis but upon realizing this might be more dimensionally challenging to work with, I decided to work with individual datasets and merge them only when needed. It should also be noted lots of the attributes are categorical hence codes are provided to indicate their respective meanings.

**Table 1**
<table>
  <tr>
    <th>Datasets</th>
    <th>Unique Identifier</th>
    <th>Number of Attributes</th>
    <th>Number of Rows</th>
  </tr>
  <tr>
    <td>Accidents</td>
    <td>Accident Index</td>
    <td>32</td>
    <td>117536</td>
  </tr>
  <tr>
    <td>Vehicles</td>
    <td>Vehicle Reference</td>
    <td>23</td>
    <td>216381</td>
  </tr>
    <tr>
    <td>Casualties</td>
    <td>Casualty Reference</td>
    <td>16</td>
    <td>153158</td>
  </tr>
</table>

## Aims 

It may sound far-fetched to suggest that certain months, days, or hours could be more dangerous. Hence, the aim of this report is to analyse UK accidents data to give insights into the following questions: 
 
(a) Are there significant hours of the day, and days of the week, on which accidents occur? <br>
(b) For motorbikes, are there significant hours of the day, and days of the week, on which 
accidents occur? <br>
(c) For pedestrians involved in accidents, are there significant hours of the day, and days of the 
week, on which they are more likely to be involved? <br>
(d) What impact, if any, does daylight savings have on road traffic accidents in the week after it 
starts and stops? <br>
(e) What impact, if any, does sunrise and sunset times have on road traffic accidents? <br>
(f) Are there particular types of vehicles (engine capacity, age of vehicle, etc.) that are more 
frequently involved in road traffic accidents? <br>
(g) Are there particular conditions (weather, geographic location, situations) that generate more 
road traffic accidents? <br>
(h) How does driver related variables affect the outcome (e.g., age of the driver, and the purpose 
of the journey)? <br>
(i) Can we make predictions about when and where accidents will occur, and the severity of the 
injuries sustained from the data supplied to improve road safety? How well do our models 
compare to government models? <br>
