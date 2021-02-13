### 读入json文件

```python
import json
#注意如果只有data = json.load("xxx.json")会报错

#AttributeError: 'str' object has no attribute 'read'

with open("xxx.json","r",encoding = "utf-8") as f:
    data = json.load(f)

#测试是否读取成功，切记不要全部打印出来，尽管有效，但是最糟糕的
print(len(data))
print(data[0])
```