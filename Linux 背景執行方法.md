# Linux 背景執行方法

其實背景執行非常簡單，只要在指令後面加個 ++**&**++

例如我要執行一個python程式，用背景執行的方式

```shell=
python main.py &
```

這樣terminal會吐回一個訊息跟你講哪個thread接了這工作

用top來檢查
```shell=
top
```

或是用ps -ef來檢查
```shell=
ps -ef
```

要殺執行緒的話，就用kill <pid>就好
```shell=
kill 324 # ex: pid = 324
```
