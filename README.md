# Learn C the Hard Way

### Intro: 
- C ir broken, which makes it ideal of techning, not good at all for writting production software.
- Main reasons C is broken: unrestricted use of pointers, and the NULL terminated string (which can be overrun).
- UB is a part of the American National Standards Institute (ANSI) C standard that lists all of the ways that a C compiler can disregard what you’ve written. There’s actually a part of the standard that says if you write code like this, then all bets are off and the compiler doesn’t have to do anything consistently. UB occurs when a C program reads off the end of a string, which is an incredibly common programming error in C.
- There’s a class of C programmers that memorized all of the UB just so they could beat up a beginner intellectually. If you run into one of these abusive programmers, please ignore them.
- Programmers attitude: assuming that nothing will work right, unless you proved that it will.

### Ex 1: Hello World. 
- Remember: sections of the man page (or manual): 1 - General command, 2 - Syscalls, 3 - libc.

### Ex 2: Make
- ```Makefile:4: *** missing separator.  Stop.``` - This and other errors can be caused by inconsistent use of tab and space.
- Example makefile:
```
CFLAGS=-Wall -g
OUTDIR=$(shell pwd)/out/
NAME=$(notdir $(shell pwd))
C_EXTENSION=.c
EXECUTABLE_EXTENSION=.exe
MACRO=
.SILENT: r  	# silence the output for the 'make run'. The echo statements are not silenced

a: cl cpl

cl: 					# make clean
	@echo "... cleaning $(OUTDIR) directory ..."
	rm -rf $(OUTDIR)

cpl:					# make compile
	@echo "... creating the output directory ..."
	mkdir $(OUTDIR)
	
	@echo "... compiling $(NAME) ..."
	cc $(CFLAGS) $(MACRO) -o $(addprefix $(OUTDIR), $(NAME))$(EXECUTABLE_EXTENSION) $(NAME)$(C_EXTENSION)
[cut]
```

### Ex 3: printf
- All printf() format specifiers: http://www.cplusplus.com/reference/cstdio/printf/
- %010d - when you want there to be 0s before the value of your variable.

### Ex 4: GDB & LLDB
- 
