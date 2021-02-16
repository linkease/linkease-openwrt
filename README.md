# openwrt-linkease
linkease for openwrt, arm and aarch64 and x86 supported

## 使用方法

把文件夹 linkease 拷贝到 Openwrt 源代码的 package/network/services 里面，拷贝之后为：

```
tree ./package/network/services/linkease
./package/network/services/linkease
├── files
│   ├── linkease.config
│   ├── linkease.init
│   └── linkease.uci-default
└── Makefile
```

