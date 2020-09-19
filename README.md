# SPEC-config
SPEC compile



### Compiler Version(gcc/g++/gfortran)

riscv
	spec06: 9.2.0
	spec17: 9.2.0

x86
	spec06: 4.8,5
	spec17: 
	

### run

spec06

*	runspec --config=???.cfg --action setup/run ???

spec17

*	runcpu  --config=???.cfg --action setup/run ???

### probleam

riscv-spec06
	ok

riscv-spec17
	unknown

x86-spec06
	unknown

x86-spec17
	intrate :  ok
	
	intspeed:  
	657:  error
	
	fprate  : ok 
	
	fpspeed :
	603:  error
	627:  error
	649:  error
	654:  error



