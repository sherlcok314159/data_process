### 读入json文件

```python
import json
with open("xxx.json","r",encoding = "utf-8") as f:
    data = json.load(f)
print(data[0])
print(len(data))
```