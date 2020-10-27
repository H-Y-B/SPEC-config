# 编译器优化选项

[QLogic PathScale Compiler Suite SPEC CPU2006 Flag Description](https://www.spec.org/cpu2006/flags/CPU2006_flags.20090714.13.html)



### -std

```
-std=c++1z           -std=f2003           -std=gnu11           -std=gnu90           -std=iso9899:1999
-std=c++03           -std=c89             -std=f2008           -std=gnu++11         -std=gnu++98         -std=iso9899:199x
-std=c11             -std=c90             -std=f2008ts         -std=gnu++14         -std=gnu99           -std=iso9899:2011
-std=c++11           -std=c++98           -std=f95             -std=gnu1x           -std=gnu9x           -std=legacy
-std=c++14           -std=c99             -std=gnu             -std=gnu++1z         -std=iso9899:1990    
-std=c1x             -std=c9x             -std=gnu++03         -std=gnu89           -std=iso9899:199409  
```

### -O1 -O2 -O3 -Os -Ofast -Og

[gcc -O1 -O2 -O3 -Os -Ofast -Og的作用](https://www.cnblogs.com/zhchy89/p/8805691.html)

-OPT:Ofast

### -ffast-math

该标记是一个群组选项，可以分别启动下面六个优化选项

* -fno-math-errno

Disables the use of the global variable errno for math functions that represent a single floating-point instruction.

* -funsafe-math-optimizations

The "unsafe math optimizations" are those that might  violate floating-point math standards, or that do away with verification of arguments and results. Using such optimizations may involve linking  code that modifies the floating-point processor's control flags.

* -fno-trapping-math

Generates "nonstop" code, on the assumption that no math exceptions will be raised that can be handled by the user program.

* -ffinite-math-only

Generates executable code that disregards infinities and NaN ("not a number") values in arguments and results.

* -fno-rounding-math

This option indicates that your program does not depend  on a certain rounding behavior, and does not attempt to change the  floating-point environment's default rounding mode. This setting is  currently the default, and its opposite, -frounding-math, is still  experimental.

* -fno-signaling-nans

This option permits optimizations that limit the number  of floating-point exceptions that may be raised by signaling NaNs. This  setting is currently the default, and its opposite, -fsignaling-nans, is still experimental.



-fb-create fbdata

-fb_opt fbdata



### -ipa (过程间分析（inter-procedural analysis）)

[编译优化之 - 过程间优化(IPA/IPO)入门](https://blog.csdn.net/qq_36287943/article/details/103930336)

### -m

These ‘-m’ switches are supported in addition to the above on x86-64 processors in 64-bit
 environments.
 -m32
 -m64
 -mx32
 -m16


 -miamcu Generate code for a 16-bit, 32-bit or 64-bit environment.

The ‘-m32’ option
 sets int, long, and pointer types to 32 bits, and generates code that runs on
 any i386 system.

 The ‘-m64’ option sets int to 32 bits and long and pointer types to 64 bits, and
 generates code for the x86-64 architecture. For Darwin only the ‘-m64’ option
 also turns off the ‘-fno-pic’ and ‘-mdynamic-no-pic’ options.


 The ‘-mx32’ option sets int, long, and pointer types to 32 bits, and generates
 code for the x86-64 architecture.


 The ‘-m16’ option is the same as ‘-m32’, except for that it outputs the
 .code16gcc assembly directive at the beginning of the assembly output so
 that the binary can run in 16-bit mode.


 The ‘-miamcu’ option generates code which conforms to Intel MCU psABI. It
 requires the ‘-m32’ option to be turned on.
 
 
 
### -g（gdb调试的时候）

默认编译生成的可执行文件是无法使用 gdb 来跟踪或调试的，因为可执行程序中没有可供 gdb 调试使用的特殊信息，为了将必要的调试信息整合到可执行文件中，我们便需要用到 -g 选项，这样生成的可执行程序，倘若出现问题，便可以使用 gdb 找出问题具体出现的位置，便于问题的解决

“-g” 标志是对程序进行调试性编译时常用的选项，我们需要给每一个需要调试的源文件都加上这个选项，它将使用特殊版本的C语言标准库完成编译和链接操作，给库函数加上程序调试方面的支持。编译器会把这些标志自动传给链接器。

加上-g选项以后，gcc在编译是会做以下额外的操作：

* 创建符号表，符号表包含了程序中使用的变量名称的列表。

* 关闭所有的优化机制，以便程序执行过程中严格按照原来的C代码进行。
