# umeng
umeng 推送 python sdk

doc: https://developer.umeng.com/docs/66632/detail/68343

使用例子


```
# Android

def android_noti():
    noti = AndroidNotification(key, secret, "customizedcast")
    noti.alias_type = "user_id"

    noti.ticker = "ticker"
    noti.title = "title"
    noti.custom = "custom"
    noti.largeIcon = "notify_icon"
    noti.icon = "notify_bg"
    noti.img = "img"

    noti.text = "message"

    noti.extra = {
        'key1': "aa",
        'key2': "key2",
    }

    noti.production_mode = False

    noti.set_alias([1, 2, 3])

    noti.send()


# ios
def ios_noti():
    noti = AndroidNotification(key, secret, "customizedcast")
    noti.alias_type = "user_id"

    noti.alert = "message"
    noti.jumpkey = "jumpkey"

    noti.extra = {
        'key1': "key1",
        'key2': "key2",
    }

    noti.production_mode = False
    noti.set_alias([1, 2, 3])

    noti.send()
```

可根据自身业务情况再进行合理封装