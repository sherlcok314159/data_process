### 热力图

热力图常用在**计算完相关性系数**之后，将计算结果进行可视化处理

```python
import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt 
import seaborn as sns

train_corr = train_data.corr()
#计算数据集中任意两个的相关性系数，返回形式与原先数据集一样
sns.heatmap(train_corr,square = True,annot = True)
#square如果为 True，则将坐标轴方向设置为"equal"，以使每个单元格为方形。
#annot如果为True，则每个单元格内填充数字
plt.show()
```

寻找与测试标签最相关的10个特征变量
```python
k = 10
cols = train_corr.nlarget(k,"target")["target"].index
#第一个target表示与target最相关的，第二个表示target那一列
#index作用变成索引对象,注意不要尾部加括号
#Index(['target', 'V0', 'V1', 'V8', 'V27', 'V31', 'V2', 'V4', 'V12', 'V16'], dtype='object')
plt.subplots(figsize = (10,10))
sns.heatmap(train_data[cols].corr(),square = True,annot = True)
plt.show()
```