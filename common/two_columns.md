### 两列操作

如果我们拿到超市几个月的销售数据，而且是完全打乱，那么**一天的购买情况分布在数据集的不同地方**，我们想按照日期排序，另外根据日期和该天销售总额来画一张折线图

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("supermarket_sales - Sheet1.csv", parse_dates=["Date"])
#关于parse，是因为日期格式如1/5/2019，会出现乱码
df_sub = df[["Total","Date"]].groupby("Date").sum().reset_index()
print(df_sub.head())

        Date      Total
0 2019-01-01  4745.1810
1 2019-01-02  1945.5030
2 2019-01-03  2078.1285
3 2019-01-04  1623.6885
4 2019-01-05  3536.6835

#按照日期进行排序，日期会出现在第一列
#sum的将分散的Total进行统计
#reset_index 是重新索引，前面有0,1,2,3,4……

sns.relplot(data = df_sub,x = "Date",y = "Total",aspect = 2,kind = "line")
plt.show()
```
