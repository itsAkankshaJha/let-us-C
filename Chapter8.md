A man cannot perform all his taks alone ,therefore he has to rely upon others to help him .We need an electrician to fix our wires , a carpenter for wooden works , a motor mechanic to repair our vehicles etc etc <br>
Similarly a computer program cannot perform all the tasks.It requests other program-like entities—called **functions** in C—to get its tasks done<br>

# FUNCTIONS:
A function is an independent block of code that performs a coherent task.:smiley: using a function is something like hiring a person to do a specific job for you<br>
- A C program can have  more than one function

       # include<stdio.h>
       void sayhello( );
       int main ()
       {  
         sayhello;
         return 0;
       }
       void sayhello( )
       {  
         printf("Hello World");
         printf("welcome to programming");
         
       }
 #### There are two types of functions : user defined functions & library functions.      
       
- If a C program contains only one function, it must be **main( )** since program execution always begins with main( ).

- When one function is called inside main , then the activity of main( ) is temporarily suspended and control goes to that function. But when function runs out of statements to execute, the control returns to main( ), which 
comes to life again and begins executing its code at the exact point where it left off. Thus, **main( )** becomes the **‘calling’ function,** whereas the **function** becomes the **called’ function**.

- Each function in a program is called in the sequence specified by the function calls in main( ).
- A function can call other functions too. **Even main( ) can be called from other functions**.
- A function can be called any number of times.
- The order in which the functions are defined in a program and the order in which they get called need not necessarily be same
- A function can call itself. Such a process is called **recursion**
- A function can be called from another function, but **a function cannot be defined in another function.**

### Why use functions ?
Why write separate functions at all? Why not squeeze the entire logic into one function, main( )? <br>

 - Writing functions avoids rewriting the same code over and over. 

- By using functions it becomes easier to write programs and keep track of what they are doing. If the operation of a program can be 
divided into separate activities, and each activity placed in a different function, then each could be written and checked more or less independently.Separating the code into modular functions also makes the program easier to design and understand

### How to write a function?
a function has three parts :
- Function declaration / Function prototype -  We declare the syntax of function before using it . Thi has inputs/parameters/ arguements a function will take or operate on 
and it also has a return type which means what output will it give.
- Function Definition : This contains the code of a function or its actual task.

- Function call : after declaring and defining our function , we can call or invoke it anywhere in our program

      # include<stdio.h>
      int sum ( int a, int b); // This is function declaration
      int main()
      {  int x=5, y=6;
         int c;
         c = sum(x,y); // this is function call
         return 0;}
         
         int sum ( int a, int b) // this is function definition
      {   int s;
          s = a+b;
          return s;
      }
  - in the above code " a and b "  are **formal parameters / formal arguements** whereas  "x and y "  are **actual parameters or actual arguements** .
   ### some important points to keep in mind while dealing with functions :sunglasses:
   -  Any number of arguments can be passed to a function being called but the type, order and number of the actual and formal arguments must always be same.
   -  It is not compulsory to use variable names in the prototype declaration
   -  The names of actual and formal parameters can be seen ,inspite of that compiler will treat both differently.
   -  If the value of a formal argument is changed in the called function,the corresponding change does not take place in the calling function ( call by value)
             
             # include <stdio.h>
              void fun ( int ) ;
              int main( )
             {
                int a = 30 ;
               fun ( a ) ;
              printf ( "%d\n", a ) ;
                 return 0 ;
             }
             void fun ( int b )
              {
               b = 60 ;
               printf ( "%d\n", b ) ;
             }
           output: 60
                   30 
            //Thus, even though the value of b is changed in fun( ), the value of a  in main( ) remains unchanged    
            
   ### The return statement
  - On executing the return statement, it immediately transfers the control back to the calling function
  - It returns the value present in the parentheses after return, to the calling function.
  - There is no restriction on the number of return statements that may be present in a function. Also, the return statement need not always be present at the end of the called function.
  - All the following are valid return statements.
  
           return ( a ) ;
           return ( 23 ) ;
            return ;
            return a+b ;
            return sum( a, b);
   - A function can return only one value at a time
                
                return ( 2,3); // these are invalid statements
                return ( x, 3);
                
                
       -------------------------------------------------------------------------     
### Order of Passing Arguments :
**In C during a function call the arguments are passed from right to left.**

-  In some function calls it doesn't matter whether the arguments are passed from left to right or from right to left.For eg , in this case
       
            fun (a, b, c, d ) ;
 - While , in some function calls, the  order of passing arguments becomes an important consideration.For eg , in this case
        
             int a = 1 ;
              printf ( "%d %d %d\n", a, ++a, a++ ) ;
              
   ###### the output of the above code is not 1 2 2
   ######   Surprisingly, it outputs 3 3 1. This is because, in C during a function call the arguments are passed from right to left. 
 
 -----------------------------------------------------------------------------------------
 ### Library Functions
 
        # include <stdio.h>
         # include <math.h>
        int main( )
        {
         float a = 0.5 ;
        float w, x, y, z ;
         w = sin ( a ) ;
         x = cos ( a ) ;
         y = pow ( a ) ;

        return 0 ;
         }
  - sin( ), cos( ), and pow( ) are library functions.They are already presnt in C library. To make use of these functions ,we need to include .h files which is discussed in     preprocessor directives.

### NOTE :

printf() can have a mismatch in the specifier given and variables in its syntax and still the compiler will not give error .But  the specifier for which variable is not provided ,it will print garbage value. <br>
And if variables are more than the specifiers given , then oly those variables/expressions will be printed whose specifiers are given.<br>

        # include <stdio.h>
           int main( )
          {
           int i = 10, j = 20 ;
           printf ( "%d %d %d\n", i, j ) ; // output - 10 20 garbagevalue
           printf ( "%d\n", i, j ) ; // output - 10
           return 0 ;
          }
