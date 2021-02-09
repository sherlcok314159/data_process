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

#查看它的参数设置，应该改为