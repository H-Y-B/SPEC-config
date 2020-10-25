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
* spec17: [aarch64-linux-gnu 7.5.0 (Linaro GCC 7.5-2019.12)](https://releases.linaro.org/components/toolchain/binaries/latest-7/aarch64-linux-gnu/)

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

### status

riscv-spec06

	compile
		ok
		416:add ‘-std=legacy’ in FORTIMIZE
	run
		unknown

riscv-spec17

	compile
	-intrate-base-test/ref
		525 ERROR: Copying input files to first run directory at ****** FAILED
	-intspeed-base-test/ref
		625 ERROR: Copying input files to first run directory at ****** FAILED
	-fprate-base-test/ref
		ok
	-fpspeed-base-test/ref
		ok
		
	run
		unknown

x86-spec06

	compile
		ok
	run
		ok

x86-spec17

	intrate :  ok
	
	intspeed:  ok
	
	fprate  :  ok 
	
	fpspeed :
	603:  error
	627:  error
	649:  error
	654:  error

arm-spec06

```
compile: 
-int-base-test/ref  
	ok
-fp-base-test/ref  
	481.wrf  undefined reference to 'nf_strerror_'
		     undefined reference to 'nf_put_vara_text_'
    undefined reference to NetCDF functions
    
run
	unknown
```

arm-spec17

```
unknown

compile:
-intrate-base-test/ref
	525 ERROR: Copying input files to first run directory at ****** FAILED
-intspeed-base-test/ref
	625 ERROR: Copying input files to first run directory at ****** FAILED
-fprate-base-test/ref
	ok
-fpspeed-base-test/ref
	ok
	
run
-intrate-base-test   unknown  
-intspeed-base-test  unknown
-fprate-base-test    unknown
-fpspeed-base-test   unknown
```

### others

sudo mount -t iso9660 cpu2017-1_0.iso ./cpu2017

wget https://www.kernel.org/pub/linux/kernel/v4.x/linux-4.20.tar.xz

https://blog.csdn.net/wlmnzf/article/details/83110433
