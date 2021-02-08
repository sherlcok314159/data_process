### 正则表达式

*3.替换*
```python
import re
s = "132#$31"
#将非数字删除
print(re.sub(r"\D", "", s))
#13231
```
