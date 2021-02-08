### 制作标签

**索引法**

*1.*

```python
labels = "ABCD"
lis = ["B","C","A","D"]
a = [labels.index(i) for i in lis]
print(a)
#[1, 2, 0, 3]
```

*2.*

```python
lis = ["B","C","A","D"]
dic = {}
for idx,i in enumerate(lis):
    dic[i] = idx
print(dic)
#{'B': 0, 'C': 1, 'A': 2, 'D': 3}
```