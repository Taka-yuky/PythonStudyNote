# Python学習ノート

## getattr, setattrの使い方

getattrの仕様
```text
getattr(object, name[, default])
```
* object...属性を取得したいオブジェクト
* name...取得したい属性
* default...属性が存在しない場合に返すデフォルト値（オプション）

```python
class MyClass:
    def __init__(self):
        self.value = 10

obj = MyClass()
print(getattr(obj, "value"))
# 10
print(getattr(obj, "missing_attr", "default_value"))
# "default_value"
```

setattrの仕様
```text
setattr(object, name, value)
```
* object...属性を設定したいオブジェクト
* name...設定したい属性
* value...属性に設定する値

```python
class MyClass:
    def __init__(self):
        self.value = 10

obj = MyClass()
setattr(obj, "value", 20)
print(obj.value)
# 20
setattr(obj, "new_attr", "Hello")
print(obj.new_attr)
# "Hello"
```

これらの親戚に、```hasattr, delattr```等がある。

## isinstance関数
isinstance関数の言語仕様
```text
isinstance(obj, classinfo)
```

* obj...対象のオブジェクト
* classinfo...objと比較するクラスの型

```python
print(isinstance(1, int))
# True

print(isinstance(1, (int, float)))
# True

print(isinstance("aaa", (int, float)))
# False

```

サブクラスであってもTrueを返す。
```python
print(isinstance(True, int))
# True
```

# リンク

[Python組み込み関数](https://docs.python.org/ja/3/library/functions.html)
[Pythonデスクリプタガイド](https://docs.python.org/ja/3/howto/descriptor.html)
