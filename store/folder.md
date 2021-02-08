### 创建文件夹

两者都是在**终端所在路径下**进行创建

*1.os库*
```python
import os
#如果路径不存在该文件
if not os.path.exists("Images"):
    os.mkdirs("Images") 
#嵌套文件

#"/"可以用来防转义
os.mkdirs("Test/t1")
#如果是系统复制过来的路径
os.mkdirs(r"F:\xxx\xxx\xxx.md")
```

这种以*os*库创建文件夹的方法的不足在于**如果存在，则会报错**

*2.ai.helper*
```python
from ai.helper import ensure_dir
ensure_dir("Images")
#关于防转义的操作与前面一样
```

这种以*ai.helper*库创建的方法**有就不进行操作，无则创建，两种情况都无伤大雅**，相对于上一种更优