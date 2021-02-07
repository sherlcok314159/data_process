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
