# arm-spec06

```
aarch64-linux-gnu 4.9.4 
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

```
arm-linux-gnueabihf 4.9.4
compile:
-int-base-test/ref  
	403.gcc error: initializer element is not constant......
-fp-base-test/ref  
	481.wrf  undefined reference to 'nf_strerror_'
		     undefined reference to 'nf_put_vara_text_'
    undefined reference to NetCDF functions
run
	unknown
```



# arm-spec17

```
aarch64-linux-gnu 7.5.0
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

```
arm-linux-gnueabihf 7.5.0
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
	unknown
```