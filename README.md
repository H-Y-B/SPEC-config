# SPEC-config
SPEC compile



### Compiler Version(gcc/g++/gfortran)

riscv
*	spec06: 9.2.0
*	spec17: 9.2.0

x86
*	spec06: 4.8,5
*	spec17: 7.5.0 
	

arm

* spec06: aarch64-linux-gnu 4.9.4 (Linaro GCC 4.9-2017.01)    arm-linux-gnueabihf 4.9.4
* spec17: [aarch64-linux-gnu 7.5.0 (Linaro GCC 7.5-2019.12)](https://releases.linaro.org/components/toolchain/binaries/latest-7/aarch64-linux-gnu/)    arm-linux-gnueabihf 7.5.0

### bug

[416.gamess STOP IN ABRT](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=69368)

[416.gamess STOP IN ABRT](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=56993)

### run

spec06

*	runspec --config=???.cfg --action setup/run ???
>   defualt: --size=ref (ref\test\train)
>            --tune=base (base\peak\all)

spec17

*	runcpu  --config=???.cfg --action setup/run ???
>   defualt: --size=ref (ref\test\train)
>            --tune=base (base\peak\all)



### others

sudo mount -o loop cpu2017-1.1.0.iso ./cpu2017

wget https://www.kernel.org/pub/linux/kernel/v4.x/linux-4.20.tar.xz

https://blog.csdn.net/wlmnzf/article/details/83110433
