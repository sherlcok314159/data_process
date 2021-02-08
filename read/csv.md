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