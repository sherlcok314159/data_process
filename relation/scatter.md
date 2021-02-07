### 散点图

散点图可对**连续**的两个值的**关系**进行可视化
```python
import matplotlib.pyplot as plt
from random import randint

#强正相关
x = [range(1,100)]
y = [range(1,100)]
plt.scatter(x,y)
plt.show()

#强负相关
x = [range(1,100)]
y = [range(-1,-100,-1)]
plt.scatter(x,y)
plt.show()

#无相关
x = [randint(1,100) for i in range(100)]
y = [randint(1,100) for i in range(100)]
plt.scatter(x,y)
plt.show()
```

*注意*

*1.* 此处的*x,y*不需要用*numpy*处理，一维列表即可

*2.* 关于参数*marker*，一般默认很好，需要可以去查官方文档

*3.* 散点图绘图时**必须成对**，且**数量变多之后就很难看清楚**   


**拓展**

可以利用相关性公式进行计算
```python
import numpy as np 
print(np.corrcoef(x,y))
```
- *0-0.09 无相关*
- *0.1-0.3 弱相关*
- *0.3-0.5 中相关*
- *0.5-1.0 强相关*

