Brief
---
OpenWrt feeds and LuCI UI for [H3C 802.1X client](https://github.com/haswelliris/h3c)

Compile
---

Compile with OpenWrt SDK

```bash
# Download OpenWrt SDK for your current platform architecture, such as ar71xx
tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
cd OpenWrt-SDK-ar71xx-*
# Clone this repo
git clone https://github.com/LGA1150/openwrt-sysuh3c.git package/openwrt-sysuh3c
# Select LuCI -> Applications -> luci-app-sysuh3c
make menuconfig
# Compile
make package/luci-app-sysuh3c/compile V=s
```

Install
---
One can locate the compiled ipk files at `bin/packages/<architecture>/base`
Upload `sysuh3c-<ver>.ipk` and `luci-app-sysuh3c-<ver>.ipk` to your router's /tmp folder, then install via opkg

Download prebuilt ipks
---
See [releases](https://github.com/LGA1150/openwrt-sysuh3c/releases)
