# 100DaysOfMachineLearning

![](https://hackernoon.com/drafts/e11c20yk.png)


*My learning log of these 100 days are [here](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/LOG.md).*



***You are always welcome to optimize or improve any resource in this repository by following [these](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/CONTRIBUTING.md) instructions.***

## Python Package:
* Numpy: *allowing us to work with multidimensional array*

* Pandas: *to organize data in tabular form and to attach descriptive labels to rows and columns*

* Matplotlib: *2D plotting library designed for visualization of numpy computations*

* Scipy: *tools for mathematics, ML, others*

* Seaborn: *high-level interface for drawing attractive statistical graphics*

* Statsmodels: *built on top of numpy and scipy, which integrates with pandas, SM provides good summaries*

* Scikit-learn or sklearn: *used ML library for below example*


## How to Save and Load ML Models:

**WHAT** On various instances, while working on developing a Machine Learning Model, 
We'll need to save our prediction models to file, and then restore them in order to reuse our previous work to.

**WHY** We need to save and restore/reload later our ML Model , so as to -

* test our model on/with new data,

* compare multiple models,

* or anything else.

**Object serialization**: This process / procedure of saving a ML Model is also known as object serialization - 
```
representing an object with a stream of bytes, in order to store it on disk, 
send it over a network or save to a database.
```
**Deserialization**: While the restoring/reloading of ML Model procedure is known as deserialization.

### Example
```
from sklearn.externals import joblib
joblib.dump(model, 'filename.pk1')                    #Save in file  
model = joblib.load('filename.pk1')                   #Load from file
```
