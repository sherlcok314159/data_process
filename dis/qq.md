### Q-Q图

Q-Q图是用来查看数据分布是否符合**正态分布**
如果点都在直线上，那么就是符合的
```python
from scipy import stats
import matplotlib.pyplot as plt

stats.probplot(train_data["V0"],plot = plt)
plt.show()
```