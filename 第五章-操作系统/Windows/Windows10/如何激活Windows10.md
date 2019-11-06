# 如何激活Windows10

```shell
#以管理员身份打开 MSDOS 窗口，输入命令：
slmgr.vbs/upk
#输入激活密钥
slmgr/ipk 密钥
# 设置系统序列号验证的服务器地址
slmgr/skms zh.us.to
#接着输入
slmgr/ato
```

**注意：**如果想还原，则输入`slmgr/ckms`

