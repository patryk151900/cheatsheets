compile with -g

in vim:
ConqueGdb --args <executable> arg1 arg2
ConqueGdb <executable>

file <file>						load symbols from file
break <function>				set breakpoint at function
break <line>					set break at line number
break <file>:<line>				set breakpoint at line in file
break <line> if <condition>		
cond 1 val>0					stop on condition 1 when condition
clear							deletes all breakpoints
disable <number>				disables bp/wp
enable <number>					enables bp/wp
delete <num>					deletes bp/wp
save breakpoints <file>			seve breakpoints
source <file>					load breakpoints

<enter>							repeat previous instruction
run								starts debug session
kill							kills process
start							set breakpoing at main and run
continue						continues the execution flow
step							step into a subroutine
finish							finish function execution and step out
next							execute next statement
return <value>					force return from function

print/<format> <variable>		prints variable
<format>						x hex, d signed decimal, u unsigned decimal, o octal, t binary, a address, c char, f floting, s string, r raw
display/<format> <var>			as print but after each execution
enable/disable display <var>	
undisplay #						remove display #
x/nfu							examine; n - how many; f format; unit: b - byte, h - 2 bytes, w - 4 bytes, g - 8 bytes
x/20i $pc						examine 20 instructions
x <variable>					low level print
x/b								examine 1 byte
x/10b							examine 10 bytes
set val=0						set varable at value

backtrace or wher				show callstack
where full						show callstack and variables
up								goes up in the call stack
down							goes down in the call stack
list							lists the code
list-							lists previous lines
list <function>					list function

watch <var>						prints variable continuosly
watch *(int *) 0x600850			watch certain
rwatch <var>					when var is being read
awatch <var>					when var is being read/write
whatis <var>					show type of the value
info args/breakpoints/display/locals/sharedlibrary/signals/threads/wathpoints
show directories/listsize

