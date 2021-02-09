### 折线图

*A.matplotlib*
```python
import matplotlib.pyplot as plt
import pandas as pd

df = pd.read_csv("supermarket_sales - Sheet1.csv")

plt.plot(df["Total"],df["Date"])
plt.show()

#需要注意的是，这里不能用x= ,y = 
plt.plot(x = df["Total"],y = df["Date"])
plt.show()
#TypeError: plot got an unexpected keyword argument 'x'

#如果改为scalex = ,scaley = 还是一样会报错
```

*B.seaborn-relplot*
```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("supermarket_sales - Sheet1.csv")
sns.relplot(data = df,x = "Total",y = "Date",kind = "line",aspect = 3)
#aspect参数可以理解为数值越大，整张图沿x轴拉伸的程度越大
plt.show()
```
