### 堆叠柱状图

```python
import pandas as pd 
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("supermarket_sales - Sheet1.csv", parse_dates=["Date"])
sns.displot(data = df,x = "Total",hue = "Gender",aspect = 3)
plt.show()

```
别忘了x即可