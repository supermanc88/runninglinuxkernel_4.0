# O0方式编译内核

[经过修改的内核](https://github.com/supermanc88/runninglinuxkernel_4.0)



环境：Ubuntu18.04

工具链：gcc5

```sh
apt-get install gcc-5
apt-get install g++-5
```



修改`_install_x86`文件夹名，不使用这个根文件系统，使用`create-image.sh`创建的文件系统。



编译：

```sh
export ARCH=x86
export CROSS_COMPILE=x86_64-linux-gnu-
make defconfig
make -j4
```

