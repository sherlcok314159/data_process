### 读入csv&tsv文件

```python
import pandas as pd 

train_data = pd.read_csv('文件路径',sep = '分隔符',nrows = '读入行数',encoding = '编码模式')

```
*注意*

*1.* 一般数据较大时，可以设置行数读入少部分

*2.* *csv,tsv*两者的分隔符分别为英文半角逗号和Tab制表符，话虽如此，但一般分隔符都是 *\\* *t*(即使有些是*txt*,数据组织格式仍如此)
***
### 基本特征
```python
train_data.info()#基本信息
print(train_data.desucribe())#main,mean,min,std等进行简单统计
print(train_data.head())#前几条数据，不一定为5
```

### 数据形式

其实读入之后是以二维矩阵形式储存的，第一个矩阵储存的为每一列的名字，如["V0","V1"……"V37","target"]，关于二维矩阵的基本元素，如*axis*,在*numpy*中已有介绍，这里也是调用的，不再赘述
```python
train_data = pd.read_csv("zhengqi_train.txt",sep = "\t",encoding = "utf-8")
print(train_data["V7"])
#为该列下的数据
print(train_data[0:1])
#为第一个矩阵
train_data["V2"].apply(lambda x : x if x <= 10 else x + 1)
#遍历某列值大于10的+1