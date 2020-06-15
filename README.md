# cvdscore (unpublish now)

The cvdscore is a python package that assists doctors to evaluate individual cardiovascular status.


## Installation and dependency package
 dependency package	
```
python >=3.6
xgboost >=0.90
```
 Installation
```
pip install cvdscore
```

## Example
```
from xgboost import XGBClassifier
import pickle
import scipy.stats as st
import pandas as pd
import numpy as np
import cvdscore
test = pd.read_table('https://raw.githubusercontent.com/VVictorChen/cvdscore/master/Example/DEMO_TESTV2.csv',sep=',',encoding='utf_8_sig')
testdata= test.drop(['result_after3year'],axis =1 ,inplace=False) 
test.head()
X = preprocess(testdata)
X.head()
cvd_age = cvdage(X)
cvd_score = main_cvdscore(X)
```











