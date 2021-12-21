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

[spec06-416.gamess STOP IN ABRT](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=69368)

[spec06-416.gamess STOP IN ABRT](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=56993)

[spec06-481:Type mismatch between actual argument at...](https://github.com/GlobalArrays/ga/issues/157)

### run

spec06

*	runspec --config=???.cfg --action setup/run ??? (int/fp/all/id)
>   defualt: --size=ref (ref\test\train)
>            --tune=base (base\peak\all)

>  "base" and "peak"
>  
>  The base metrics (e.g. SPECint_base2006) are required for all reported results and have stricter guidelines for compilation. For example, the same flags must be used in the same order for all benchmarks of a given language. This is the point closer to those who might prefer a relatively simple build process.
>  
>  The peak metrics (e.g. SPECint2006) are optional and have less strict requirements. For example, different compiler options may be used on each benchmark, and feedback-directed optimization is allowed. This point is closer to those who may be willing to invest more time and effort in development of build procedures.

> "rate" and "speed"
> 
> The SPECspeed metrics (e.g., SPECint2006) are used for comparing the ability of a computer to complete single tasks.
> 
> The SPECrate metrics (e.g., SPECint_rate2006) measure the throughput or rate of a machine carrying out a number of tasks.
> 
> For the SPECrate metrics, multiple copies of the benchmarks are run simultaneously. Typically, the number of copies is the same as the number of CPUs on the machine, but this is not a requirement. For example, it would be perfectly acceptable to run 63 copies of the benchmarks on a 64-CPU machine (thereby leaving one CPU free to handle system overhead).
> 
> --rate [copies] Synonym: -r
> 
> Default: SPECspeed run (i.e. non-rate)
> 
> Meaning: Select SPECrate run instead of SPECspeed. If a parameter is supplied, it specifies the number of copies to run. (This is identical to specifying the number of copies to run via the --copies command-line switch (which see for some important additional detail). For example, the following commands both would do a 4-copy SPECint_rate2006 run:
> 
> runspec --config=???.cfg --rate 4 int
> 
> runspec --config=???.cfg --rate --copies 4 int



spec17

*	runcpu  --config=???.cfg --action setup/run ???（'fprate', 'fpspeed', 'intrate', 'intspeed' or 'all','id'）
>   defualt: --size=ref (ref\test\train)
>            --tune=base (base\peak\all)

> There are several different ways to measure computer performance:
> 
> One way is to measure how fast the computer completes a single task; this is a speed measure. 
> 
> Another way is to measure how many tasks a computer can accomplish in a certain amount of time; this is called a throughput, capacity or rate measure.


### others

sudo mount -o loop cpu2017-1.1.0.iso ./cpu2017

wget https://www.kernel.org/pub/linux/kernel/v4.x/linux-4.20.tar.xz

https://blog.csdn.net/wlmnzf/article/details/83110433
