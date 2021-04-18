



## ORM利用時に、QuerySetのメソッドとしてlatestを利用したい場合、Meta sub classを追加して`get_latest_by`プロパティを持たせる。
```py

class Context(models.Model):
    session_id = models.CharField(max_length=64, null=False)
    
    ...

    class Meta:
        get_latest_by = ["updated_at"]
```


