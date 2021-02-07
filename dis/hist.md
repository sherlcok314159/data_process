### 直方图

```python
import matplotlib.pyplot as plt

plt.hist(x = '需要处理的数据',bins = '需要分割的精度')
plt.xlabel('x轴标签')
plt.ylabel('y轴标签')
plt.title('总标题')
plt.show()
```

*bins?*

按照我的个人实验结果，应该是关于精度的变量，**跟组数无关**

不妨*bins = 10 or 100 or 120 or 1200*对比观察一下

以下是我的个人数据

![](https://github.com/sherlcok314159/data_visualization/blob/main/Images/hist.png)

可见*bins*越大，那么**细分的程度越高**