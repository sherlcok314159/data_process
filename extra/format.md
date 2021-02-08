### 字符串格式化

*1.format*
```python
a,b = 0,1
print("{} + {} = {}".format(a,b,a+b))
# 0 + 1 = 1
```
当然关于format的用法还有很多

*2.f*
```python
a,b = 0,1
print(f"{a} + {b} = {a + b}")
# 0 + 1 = 1
```
*3.%d,%s*
```python
a,b = 0,1
print("%d + %d = %d"%(a,b,a+b))
# 0 + 1 = 1
```

*注意*

如果里面是字符串得用 *%s*,浮点数 *%f*
