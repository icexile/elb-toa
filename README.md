# 修改说明

- 本版本 folk 自 https://github.com/huaweicloud/elb-toa
- 结合了下述工作：
    - 适配 kernel 4.17 以上版本 inet_getname 函数签名变动：https://github.com/dongzerun/TCP_option_address
    - 适配 kernel 5.7 以上版本不再导出 kallsyms_lookup_name 函数： https://github.com/h33p/kallsyms-mod

因此本版本 TOA 兼容至内核主线最新版本，在生产环境验证无误。


下面是原始说明：
# TCP Option Address

The TCP Option Address (TOA) module is a kernel module that obtains the source IPv4 address from the option section of a TCP header.

## How to use the TOA module?

### Requirement

The development environment for compiling the kernel module consists of: 
- kernel headers and the module library
- the gcc compiler
- GNU Make tool

### Installation

Download and decompress the source package:
```
https://github.com/Huawei/TCP_option_address/archive/master.zip
```

Enter the source code directory and compile the module:
```
cd src
make
```

Load the kernel module:
```
sudo insmod toa.ko
```

## Distribution license

TOA is distributed under the terms of the GNU General Public License v2.0. The full terms and conditions of this license are detailed in the LICENSE file.