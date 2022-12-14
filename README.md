# Aleksana自用Matrix贴纸包

## 预览

可以在[这里](https://aleksanaa.github.io/mystickerpicker/web/)

## 我也想用！

这个picker只支持Element (Web, Electron, Android, iOS) 客户端以及基于它的客户端。

在你的Element (Web或) 的任意聊天窗口输入`/devtools`并发送，会打开一个Developer Tools窗口，在其中选择Explore account data，在其中找到m.widgets，在"content"中添加如下内容：

```
"stickerpicker": {
    "content": {
        "type": "m.stickerpicker",
        "url": "https://aleksanaa.github.io/mystickerpicker/web/?theme=$theme",
        "name": "Stickerpicker",
        "data": {}
    },
    "sender": "@you:matrix.server.name",
    "state_key": "stickerpicker",
    "type": "m.widget",
    "id": "stickerpicker"
}
```
其中sender可以保持原状，不影响使用。

如果没有找到m.widgets，就直接选择右下角Send custom account data event，event type选择m.widgets，并填入：

```
{
  "type": "m.widgets",
  "content": {
    "stickerpicker": {
      "content": {
        "type": "m.stickerpicker",
        "url": "https://aleksanaa.github.io/mystickerpicker/web/?theme=$theme",
        "name": "Stickerpicker",
        "data": {}
      },
      "sender": "@you:matrix.server.name",
      "state_key": "stickerpicker",
      "type": "m.widget",
      "id": "stickerpicker"
    }
  }
}
```

## 我还想加别的！

那你自己搭建[原版](https://github.com/maunium/stickerpicker)吧。