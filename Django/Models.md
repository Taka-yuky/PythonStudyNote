# Django Modelsに関するノート

## マネージャ

## データベース
Modelクラス内のMetaを利用してデータベースのインデックスを貼ることができる。
```python
from django.db import models

class ModelA(models.Model):
    class Meta:
        constraints = [
            models.UniqueConstraint(fields=['field1', 'field2'], name="constraint_name"),
        ]
```

# リンク

* [Django マネージャー](https://docs.djangoproject.com/ja/5.1/topics/db/managers/)
