### 箱型图

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (4,6))#分配宽度和高度
sns.boxplot('需要处理的数据',width = 0.5(矩形宽度))#默认是x = data
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

****

**绘制多个子图**

```python
columns = train_data.columns.tolist()
plt.figure(figsize = (60,80),dpi = 75)#设置整张图大小及分辨率
for i in range(38):
    plt.subplot(8,5,i+1)#8行五列，后一个参数表示第几个，不能少
    sns.boxplot(y = train_data[columns[i]],width = 0.5)
plt.show()
```

*注意*

分成几行几列要考虑

*1.* 乘积必须大于等于元素个数

*2.* 对于垂直绘图而言，y轴是标签，如果列数太多，则会导致标签插入别的图中，所以要适当调整比例(水平绘图同理)