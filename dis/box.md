### 箱型图

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (4,6))#分配宽度和高度
sns.boxplot('需要处理的数据')
plt.xlabel('x轴标签')
plt.ylabel('y轴标签')
plt.title('总标题')
plt.show()
```

![](https://github.com/sherlcok314159/data_process/blob/main/Images/box.jpg)

*注意*

**seaborn**不是python自带的第三方库，需要
终端里安装
```python
pip install seaborn
```
