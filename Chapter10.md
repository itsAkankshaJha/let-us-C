# Recursion

 When a function calls itself within its body ,then it is called as **recursive function** and this feature of C is known as recursion .
 Example of recursion:
 
 **Factorial**
  
       int factorial ( int ) 
       {
        int f = 1, i ;
        for ( i = x ; i >= 1 ; i-- )
        f = f * i ;
        return f ;
       }
    
**Recursive Function:**
     
     int fact ( int x )
     {
       int f ;
      if ( x == 1 )
      return 1 ;
      else
      f = x * fact ( x - 1 ) ;
      return f ;
     }
     
  #### Brief explanation: 
  In case the value of a is 5, main( ) would call fact( ) with 5 as its actual argument, and fact( ) will send back the computed value. But before sending the computed value, fact( ) calls fact( ) and waits for a value to be 
returned. It is possible for the fact( ) that has just been called to call yet another fact( ), the argument x being decreased in value by 1 for each of 
these recursive calls.

![Let us C pdf - Personal - Microsoft​ Edge 08-06-2021 05_57_52 PM](https://user-images.githubusercontent.com/72215893/121185518-c5d0d280-c883-11eb-8cee-2ea96f53012b.png)

 **These successive invocations of the same function are possible because the C compiler keeps track of which invocation calls** .
 
 ### Recursion and Stack 
 There are different ways in which data can be organized.  All these different ways of organizing the data are known as **data structures**.The compiler 
uses **stack (LIFO data structure)** for implementing normal as well as recursive function calls .<br>
You can compare this to the stack of plates in a cafeteria—the last plate that goes on the stack is the first one to get out of it.<br>

         #include<stdio.h>
         int add ( int i, int j )
          {
           int sum ;
          sum = i + j ;
           return sum ; 
          }
          int main( )
          {
          int a = 5, b = 2, c ;
          c = add ( a, b ) ;
          printf ( "sum = %d\n", c ) ;
          return 0 ;
         }
 
  #### The recursive calls are no different. Whenever we make a recursive call the parameters and the return address gets pushed on the stack. The stack gets unwound when the control returns from the called function. Thus during every recursive function call we are working with a fresh set of parameters.
   As shown below:
   - In this program, before transferring the execution control to the function add( ), the values of parameters a and b are pushed on the stack.
   - then the address of the print() is pushed in the stack.
   - and the control is transferred to add( ). 
   - . Once inside add( ), the local variable sum gets pushed on the stack .
   - When value of sum is returned,sum is popped off from the stack. 
   - Next, the address of the statement where the control should be returned, is popped off from the stack. 
   - Using this address, the control returns to the printf( ) statement in main( ). Before execution of printf( ) begins, the two integers that were earlier pushed on the stack are now popped off.
   
   ### NOTE
 popping of sum and address is done by add( ), whereas, popping of the two integers is done by main( ). When it is done this way, it is known as ‘cdecl Calling Convention’. There are other 
 calling conventions as well, where instead of main( ), add( ) itself clears the two integers. The calling convention also decides whether the parameters being passed to the function are pushed on the stack in leftto-right or right-to-left order. The standard calling convention always 
 uses the right-to-left order. 
 
 ![Let us C pdf - Personal - Microsoft​ Edge 08-06-2021 06_20_40 PM](https://user-images.githubusercontent.com/72215893/121188119-6cb66e00-c886-11eb-9ea8-b35a1f6402a6.png)


