# openwrt-v2ray

基于[kuoruan/openwrt-v2ray](https://github.com/kuoruan/openwrt-v2ray), 兼容 `luci-app-ssr-plus` 的 v2ray 软件包.

## 使用方法:

直接替换 `package/lean/v2ray`

(仅适用于 [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede) 及自行添加 `luci-app-ssr-plus` 的 OpenWrt 固件)

### 修改点:

- 兼容 `luci-app-ssr-plus` :
  - 修改包名为 `v2ray` .
  - 更改二进制安装位置到 `/usr/bin/v2ray/` .
- 裁剪软件包体积:
  - 默认不包含 `v2ctl` .
  - 如果是小内存设备, 会调用 upx 来对二进制文件进行压缩.
