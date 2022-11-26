# how to build 

准备编译环境参考： http://confluence.mmcuav.com:8002/pages/viewpage.action?pageId=29261923

下载源码，解压到这个路径
Linux_for_Tegra/source/public


会自动替换对应的修改

然后编译

```

cd Linux_for_Tegra/source/public/kernel/kernel-4.9
export CROSS_COMPILE=/opt/gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu- && make ARCH=arm64  O=~/nvidia/product tegra_defconfig
export CROSS_COMPILE=/opt/gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu- && make ARCH=arm64  O=~/nvidia/product -j8
export CROSS_COMPILE=/opt/gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu- && make ARCH=arm64 O=~/nvidia/product modules_install INSTALL_MOD_PATH=~/nvidia/product/modules
```
