# 用Python的numpy包实现softmax函数

Softmax函数如下图所示： 
 
![softmax](./imgs/softmax.PNG)

```
import numpy as np
def softmax(x):
    return np.exp(x)/np.sum(np.exp(x),axis=0)
    
```
