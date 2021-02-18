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

**需要注意，只是组织形式在概念上与矩阵相似，矩阵的切片它不能用**
```python
train_data = pd.read_csv("zhengqi_train.txt",sep = "\t",encoding = "utf-8")
print(train_data["V7"])
#为该列下的数据
print(train_data[0:1])
#为第一个矩阵
print(train_data[:,0:1]
#TypeError: '(slice(None, None, None), slice(0, 1, None))' is an invalid key
train_data["V2"] = train_data["V2"].apply(lambda x : x if x <= 10 else x + 1)
print(train_data["V2"])
#遍历某列值大于10的+1

#注意，更改了之后要重新赋一个，类似于字符串的操作
```

### 基础操作

```python
import pandas as pd 
data = pd.read_csv(path)
print(data.head())
#
   id    tid1...   title2_en      label        
0   0     0  ...  Police...  unrelated
1   3     2  ...  Shenzhen...  unrelated
2   1     2  ...  The GDPi...  unrelated
3   2     2  ...  Shenzhen...  unrelated
4   9     6  ...  It took...     agreed
#

#取某一列,e.g."label"
print(data["label"])
#取第一行和第一列交汇处的值
print(data.loc[0,"id"])

#loc根据行和列标签进行索引，左边为行，右边为列，中间以","隔开

#取第一行和第一列，第二列交汇处的值
print(data.loc[0,"id":"tid1"])

#注意，这里的是全闭合的，后面不是开放的

print(data.loc[0, ["id", "tid1"]])
#与上面结果一致

#取第一行
print(data.loc[0])

#取某几列
print(data.loc[:,["label","id"]])

#iloc与loc不同，是基于行索引和列索引的，从0开始

#取第一行和第一列交汇处的值
print(data.iloc[0,0])

#语法与loc相同，唯一不同只是把标签变为了索引，这里不再赘述

#创建新的一列
data["new"] = data["label"].apply(lambda x:x+1)
