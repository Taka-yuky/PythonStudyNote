# Numpyに関するノート

## 配列の作り方

```python
import numpy as np
array = np.array(12)
```

## 配列の次元の確認

```python
import numpy as np
array = np.array(12)

print(array.ndim)
# 0

array = np.array([1, 2, 3, 4])
print(array.ndim)
# 1
```

## 配列の型の確認
```numpy```のarray型では同じarray内では同じ型しか用いることができない。

```python
import numpy as np
array = np.array([1, 2, 3, 4])
print(array.dtype)
```
## ゼロ埋めされた任意のm×n行列を作る

```python
import numpy as np
array = np.zeros((300, 20))
```

## 行列を転置させる

```python
import numpy as np
array = np.zeros((300, 20))

array = np.transpose(array)
print(array.shape)
# (20, 300)
```
