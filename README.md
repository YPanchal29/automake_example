# automake_example

1. create c code file 
2. create configure.ac
3. create Makefile.am 

- Put necessary code in the c files
- =========================================================================================
- configure.ac 
- =========================================================================================
  AC_INIT([sample],[0.1],[ypblacksmith95@gmail.com])

  AM_INIT_AUTOMAKE

  AC_PROG_CC

  AC_CONFIG_FILES([Makefile])

  AC_OUTPUT
=========================================================================================

=========================================================================================
- Makefile.am 
- =======================================================================================
bin_PROGRAMS = sample
sample_SOURCES = sample.c

=========================================================================================
commands to be follow 
=========================================================================================
- aclocal 
- autoheader
- automake -> some error will display 
- touch NEWS
- touch INSTALL
- touch AUTHORS
- touch ChangeLog
- touch README

- automake --add-missing
- autoconf
- ./configure

following logs you will get it 
=========================================================================================
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... no
checking for mawk... mawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: executing depfiles commands

=========================================================================================

- make clean
- make  
- binary is ready 
- make dist - Output ->  sample-0.1.tar.gz
- Take this tar buddle and keep any other place
- ./configure
- make 
- binary is ready 
