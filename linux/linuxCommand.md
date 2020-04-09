1. chown: 修改文件拥有者组

```linux
chown -R root:root *
# 将当前目录下所有文件用户设为root组root; -R指定目录及其子目录下所有文件
```

2. chmod: 修改文件权限

```linux
chmod ugo+rwx file.txt
# 将文件设定为所有人均可读写执行
# u--拥有者; g--组; o--其它用户; r--读; w--写; x--执行
```

   

   