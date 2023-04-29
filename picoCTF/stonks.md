https://www.youtube.com/watch?v=2gnaG4ocGLA&t=722s

STONKS

we exploit the print formatting vuln here.
If the programmer passes an attacker-controlled buffer as an argument to a printf (or any of the related functions, including sprintf, fprintf, etc)
, the attacker can perform writes to arbitrary memory addresses.
Since printf has a variable number of arguments, it must use the format string to determine the number of arguments. In the case above, 
the attacker can pass the string “%p %p %p %p %p %p %p %p %p %p %p %p %p %p %p” and 
fool the printf into thinking it has 15 arguments. It will naively print the next 15 addresses on the stack.

The Format String exploit occurs when the submitted data of an input string is evaluated as a command by the application. In this way, the attacker could execute code, read the stack, or cause a segmentation fault in the running application, causing new behaviors that could compromise the security or the stability of the system.

To understand the attack, it’s necessary to understand the components that constitute it.

•The Format Function is an ANSI C conversion function, like printf, fprintf, which converts a primitive variable of
the programming language into a human-readable string representation.

•The Format String is the argument of the Format Function and is an ASCII Z string which contains text 
and format parameters, like: printf (“The magic number is: %d\n”, 1911);

•The Format String Parameter, like %x %s defines the type of conversion of the format function.


Safe Code

The line printf("%s", argv[1]); in the example is safe, if you compile the program and run it:

./example "Hello World %s%s%s%s%s%s"

The printf in the first line will not interpret the “%s%s%s%s%s%s” in the input string, and the output will be: “Hello World %s%s%s%s%s%s”


Vulnerable Code

The line printf(argv[1]); in the example is vulnerable, if you compile the program and run it:

./example "Hello World %s%s%s%s%s%s"
