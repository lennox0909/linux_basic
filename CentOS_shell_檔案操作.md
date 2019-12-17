# CentOS shell 檔案操作

## CentOS install unzip
```shell=
sudo yum install unzip
```
將壓縮檔所有檔案解壓到指定目錄, 可以用 -d 參數設定, 以下假設解壓到 /home/phpini
```shell=
unzip file.zip -d /home/phpini
```
## Linux 開啟檔名有空格的檔案
* 如果有一個檔案名為 “file name.txt”, 在 Linux 要開啟有以下兩種方法, 分別是用引號包著檔案名稱, 以反在空格前加入 “\” 字符
```shell=
cat ‘file name.txt’
# or
cat file\ name.txt
```

## 重新命名(rename) & 新增檔案(new file)的指令

將a.txt改名稱為b.out
```shell=
mv a.txt b.out
```

新增檔案a.txt
```shell=
touch a.txt
```

## 批次修改檔名

當一個目錄資料夾底下有很多有特定規則檔名的檔案需要改名，
例如相機產生的檔案 IMG001.jpg~IMG999.jpg 超多檔案，
這絕對不可能直接用 mv 一個個慢慢敲來改名的。
這時候另一個指令就可以派上用場了，
rename 這個指令可以用來批次修改檔名共同的部分，使用方式如下：
```shell=
rename $1 $2 $3
 $1: 要被取代的關鍵字
 $2: 新的關鍵字
 $3: 檔名符合這個規則的才取代
```


把 IMG001.jpg, IMG002.jpg… 換成 img001.jpg, img002.jpg… 
```shell=
rename IMG img IMG*
```

把所有 .htm 檔案改成 .html
```shell=
rename .htm .html *.htm
```


把檔案 foo1, ..., foo9, foo10, ..., foo278.
改成 foo001, ..., foo009, foo010, ..., foo278.
```shell=
rename foo foo0 foo?
rename foo foo0 foo??
```


## rm – 刪除檔案及目錄指令

rm 的使用也很簡單, 只要在指令後面加入檔案名稱, 便可以將檔案刪除, 例如:


```shell=
rm filename
```


但如果要刪除目錄, 像上面直接輸入的話, 會出現報錯:


```shell=
rm dirname/
rm: cannot remove ‘dirname/’: Is a directory
```
要刪除目錄, 需要加入 -r 參數, -r 參數代表 recursive 遞迴刪除, 使用時要格外小心, 因為會把目錄內所有檔案及目錄一同刪除:


```shell=
rm -r dirname/
```
如果要刪除空目錄, 可以用 -d 參數, 但如果目錄內有檔案或副目錄便不能刪除:



```shell=
rm -d dirname/
```

刪除前會先詣問, 可以避免操作錯誤, Redhat 預設會用這個參數:


```shell=
rm -i filename
```
強制刪除, 不會有任何警告, 使用時要小心:


```shell=
rm -f filename
```
在 Linux 有一部指令很危險, 也常被人拿作開玩笑, 就是加入 -r 及 -f 參數, 將整個 “/” 根目錄刪除而不會先警告:


```shell=
rm -rf /
```
但各發行版為了安全起見, 輸入以上指令已經不能生效了。但如果真的想砍掉整個根目錄, 可以用以下兩種指令:

```shell=
rm -rf –no-preserve-root /
或
rm -rf /*
```

## Linux 如何查看 系統硬體 的 詳細記憶體(RAM)資訊

```shell=
free

## 以 MB 作為單位顯示記憶體使用狀況
free -m

## 以 GB 作為單位顯示記憶體使用狀況
free -g


cat /proc/meminfo

## 要查詢詳細的 RAM 規格, ex: DDR2、DDR3 .. 等, 可以用下述指
sudo lshw

## 執行 top 指令後, 可以從 “Mem:” 及 “Swap:” 兩行看到記憶體及 SWAP 的使用狀況
top
```

## 檢查硬碟使用量 df
df -hl 查看磁盤剩餘空間
df -h 查看每個根路徑的分區大小
```shell=
## 檢查硬碟使用量
df

## 以容易閱讀的方式顯示
df -h

## 顯示檔案系統
df -T

## 指定要顯示的檔案系統
df -t vfat ## 類型

## 指定要排除顯示的檔案系統
df -x vfat ## 類型
```

## 檢查目錄大小 du (disk usage)
du -sh [目錄名] 返回該目錄的大小
du -sm [文件夾] 返回該文件夾總M數
