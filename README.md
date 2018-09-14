# Learn-C-The-Hard-Way

## Notes:
- C ir broken, which makes it ideal of techning, not good at all for writting production software.
- Main reasons C is broken: unrestricted use of pointers, and the NULL terminated string (which can be overrun).
- UB is a part of the American National Standards Institute (ANSI) C standard that lists all of the ways that a C compiler can disregard what you’ve written. There’s actually a part of the standard that says if you write code like this, then all bets are off and the compiler doesn’t have to do anything consistently. UB occurs when a C program reads off the end of a string, which is an incredibly common programming error in C.
- 
