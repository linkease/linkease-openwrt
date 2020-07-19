# openwrt-linkease
linkease for common openwrt, arm and x86 supported

## ARM 使用方法

```
curl -XGET https://firmware.koolshare.cn/binary/LinkEase/LinuxStorage/linkease.arm ./linkease/files/link-ease
chmod 755 ./linkease/files/link-ease
cp -rf ./linkease package/network/utils/
```

## X86 使用方法

```
curl -XGET https://firmware.koolshare.cn/binary/LinkEase/LinuxStorage/linkease.amd64 ./linkease/files/link-ease
chmod 755 ./linkease/files/link-ease
cp -rf ./linkease package/network/utils/
```

