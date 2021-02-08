### 计数

*1.列表自带*
```python
lis = [1, 2, 3, 2, 3, 3, 32, 1, 35, 54, 3]
print(lis.count(3))
#4
```

*2.Counter*
```python
from collections import Counter

lis = [1, 2, 3, 2, 3, 3, 32, 1, 35, 54, 3]
a = Counter(lis)
print(a)
#Counter({3: 4, 1: 2, 2: 2, 32: 1, 35: 1, 54: 1})
# 需要注意的是，这种分类方法是将次数降序排列
print(type(a))
#<class 'collections.Counter'>
# 返回Counter类
for x, y in a.items():
    print(x, y)
#1 2
#2 2
#3 4
#32 1
#35 1
#54 1
# 可以作为字典遍历
```

*3.字典法*
```python
lis = [1, 2, 3, 2, 3, 3, 32, 1, 35, 54, 3]
dic = {}
for i in lis:
    dic[i] = dic.get(i,0) + 1
print(dic)
#{1: 2, 2: 2, 3: 4, 32: 1, 35: 1, 54: 1}
#按照元素排列
```