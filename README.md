<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="EDATitanic_Dataset_0"></a>EDA-Titanic Dataset</h1>
<h2 class="code-line" data-line-start=1 data-line-end=2 ><a id="using_python_and_its_libraies_1"></a>using python and it’s libraies</h2>
<h5 class="code-line" data-line-start=4 data-line-end=5 ><a id="What_is_EDA_4"></a>What is EDA?</h5>
<p class="has-line-data" data-line-start="5" data-line-end="7">Exploratory Data Analysis (EDA) is a method used to analyze and summarize datasets. Majority of the EDA techniques involve the use of graphs…<br>
The csv file can be downloaded from <a href="https://www.kaggle.com/c/titanic/data">Kaggle</a>.</p>
<h5 class="code-line" data-line-start=8 data-line-end=9 ><a id="Titanic_Dataset__8"></a>Titanic Dataset –</h5>
<p class="has-line-data" data-line-start="9" data-line-end="10">It is one of the most popular datasets used for understanding machine learning basics. It contains information of all the passengers aboard the RMS Titanic, which unfortunately was shipwrecked. This dataset can be used to predict whether a given passenger survived or not.</p>
<h5 class="code-line" data-line-start=11 data-line-end=12 ><a id="The_dataset_11"></a>The dataset</h5>
<ol>
<li class="has-line-data" data-line-start="12" data-line-end="13">PassengerID : unique Id of a passenger</li>
<li class="has-line-data" data-line-start="13" data-line-end="14">Survived :if the passenger survived (0-No, 1-Yes)</li>
<li class="has-line-data" data-line-start="14" data-line-end="15">Pclass : Passeneger Class (1= 1st,2= 2nd,3= 3rd)</li>
<li class="has-line-data" data-line-start="15" data-line-end="16">Name : Name of the passenger</li>
<li class="has-line-data" data-line-start="16" data-line-end="17">Sex : Male/Female</li>
<li class="has-line-data" data-line-start="17" data-line-end="18">Age : Passenger age in years</li>
<li class="has-line-data" data-line-start="18" data-line-end="19">SibSp : No.of siblings/spouses aboard</li>
<li class="has-line-data" data-line-start="19" data-line-end="20">Parch: No. of parents/children aboard</li>
<li class="has-line-data" data-line-start="20" data-line-end="21">Tickets: Ticket Nuumber</li>
<li class="has-line-data" data-line-start="21" data-line-end="22">Fare: Passeneger Fare</li>
<li class="has-line-data" data-line-start="22" data-line-end="23">Cabin: Cabin No.</li>
<li class="has-line-data" data-line-start="23" data-line-end="24">Embarked: Port of Embarkation (C= Cherbourg; Q= Queenstown;S= SOuthampton)</li>
</ol>
<h3 class="code-line" data-line-start=27 data-line-end=28 ><a id="Importing_libraries_27"></a>Importing libraries</h3>
<h5 class="code-line" data-line-start=30 data-line-end=31 ><a id="Pandas_30"></a>Pandas:</h5>
<p class="has-line-data" data-line-start="31" data-line-end="32">It provides in memory 2d table object known as dataframe. It is like  a spreedsheet with column names and row label.Hence, pandas is capable of providing many addittional functionalilties like creating pivot tables, computing columns based on other columns and plotting graphs</p>
<h5 class="code-line" data-line-start=33 data-line-end=34 ><a id="Numpy_33"></a>Numpy:</h5>
<p class="has-line-data" data-line-start="34" data-line-end="36">NumPy stands for ‘Numerical Python’ or ‘Numeric Python’.<br>
It is an open source module of Python which provides fast mathematical computation on arrays and matrices.</p>
<h5 class="code-line" data-line-start=37 data-line-end=38 ><a id="Matplotlib_37"></a>Matplotlib:</h5>
<p class="has-line-data" data-line-start="38" data-line-end="40">Matplotlib is a 2d plotting library which produces publication quality figures.<br>
Matplotlib can be used in Python scripts, Python and IPython shell, Jupyter Notebook, web application servers and GUI toolkits. matplotlib.pyplot is a collection of functions that make matplotlib work like MATLAB.</p>
<h5 class="code-line" data-line-start=41 data-line-end=42 ><a id="Seaborn_41"></a>Seaborn:</h5>
<p class="has-line-data" data-line-start="42" data-line-end="44">It is a python library used to statistically visualize data. Seaborn, built over Matplotlib, provides a better interface and ease of usage. It can be installed using the following command,<br>
pip3 install seaborn.</p>
<pre><code>import pandas as pd 
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
</code></pre>
<h4 class="code-line" data-line-start=56 data-line-end=57 ><a id="Features_The_titanic_dataset_has_roughly_the_following_types_of_features_56"></a>Features: The titanic dataset has roughly the following types of features:</h4>
<ul>
<li class="has-line-data" data-line-start="57" data-line-end="58">Categorical/Nominal: Variables that can be divided into multiple categories but having no order or priority. Eg. Embarked (C = Cherbourg; Q = Queenstown; S = Southampton)</li>
<li class="has-line-data" data-line-start="58" data-line-end="59">Binary: A subtype of categorical features, where the variable has only two <a href="http://categories.Eg">categories.Eg</a>: Sex (Male/Female)</li>
<li class="has-line-data" data-line-start="59" data-line-end="61">Ordinal: They are similar to categorical features but they have an order(i.e can be sorted).<br>
Eg. Pclass (1, 2, 3)</li>
<li class="has-line-data" data-line-start="61" data-line-end="63">Continuous: They can take up any value between the minimum and maximum values in a column.<br>
Eg. Age, Fare</li>
<li class="has-line-data" data-line-start="63" data-line-end="65">Count: They represent the count of a variable.<br>
Eg. SibSp, Parch</li>
<li class="has-line-data" data-line-start="65" data-line-end="66">Useless: They don’t contribute to the final outcome of an ML model. Here, PassengerId, Name, Cabin and Ticket might fall into this category.</li>
</ul>
