# UCloud PathX TOA kernel module


## Install module on Amazon Linux
```bash
yum install gcc
yum install kernel-headers
yum install kernel-devel
yum install kernel-devel-$(uname -r)

git clone https://github.com/lenew/toa.git
cd toa
make

mv toa.ko /lib/modules/`uname -r`/kernel/net/netfilter/ipvs/toa.ko
insmod /lib/modules/`uname -r`/kernel/net/netfilter/ipvs/toa.ko
lsmod | grep toa
```