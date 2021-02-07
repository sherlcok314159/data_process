### 提琴图

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (6,6))
sns.violinplot(x = '数据')#可以自己设置哪个轴
plt.xlabel('x轴标签')
plt.ylabel('y轴标签')
plt.title('大标题')
plt.show()
```

提琴图结合了箱型图和概率分布

*median(中位数)：* 中间的白色空心

