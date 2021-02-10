### 核密度分布图

```python
import matplotlib.pyplot as plt
import seaborn as sns

ax = sns.kdeplot(train_data["V0"],color = "Red",shade = True)
ax = sns.kdeplot(test_data["V0"],color = "Blue",shade = True)
ax.legend(["Train","Test"])
plt.show()
```

核密度曲线分布预测可以用来**查看训练和测试所用的数据分布是否一致**，如果差别太大，会导致泛化能力变差，因而舍弃