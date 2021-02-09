### 直方图

*A.matplotlib——普通直方图*
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

可见*bins*越大，那么**细分的程度越高**，然而细分到一定程度，单个条柱的高度则**易受采样误差的影响**，容易被**噪音干扰**

所以个人意见是

***在一定范围内尝试更改bins,保证在精细化的前提不会太容易受到噪音干扰***

*B.sns-displot——带拟合曲线的直方图*
```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.displot(d["Total"],kde = True,bins = 50)
#kde就是拟合曲线的设置
#bins参数与上面一致
plt.show()
```

关于直方图，默认*x轴*为数据，*y轴*默认为*计数*

**拟合曲线**可以较精确地反映整个直方图的趋势

同样，*sns*绘图自带标签，颜值也高一点，其实，**seaborn**是对**matplotlib**的再次封装