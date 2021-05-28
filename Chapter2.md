  # C Instructions <br>
   :jigsaw: A program is a set of **instructions**.<br>
  :abacus: Three types of instructions in C :abacus::<br>
:diamonds: Type Declaration Instruction –  to declare the type of variables used in a C program.<br>
any variable that we are using in our program needs to be declared first.<br>
- we can declare & initialize a varibale > int a = 9 ; float b = 3+ 0.5 ; <br>
- The order in which we define the variables is sometimes important sometimes not. <br>
- we cannot use *a* before defining it<br>
-      int b = a + 5; 
-      int a = 0 ; 
This will work <br>
-      int a,b,c ;
-      a=b=c=10;
but  will give error<br>
-      int a=b=c= 10 ;
:diamonds: Arithmetic Instruction – to perform arithmetic operations on constants and variables.<br>
- It consists of a variable name on LHS of = and variable names , arithmetic operator or sconstants on RHS  of = <br>
An arithmetic instruction could be of 3 types : integer mode ,real mode and mixed mode<br>
:smiley:C allows only one variable on left-hand side of =. That is,**z = k * l** is legal, whereas **k * l = z** is illegal. </br>
:smiley: MODULUS OPERATOR : only operates on integers , gives the remainder of two numbersa after division , the **sign** is always the sign of numerator <br>
:slightly_smiling_face: -5 % 2 = –1, whereas, 5 % -2 = 1 :upside_down_face: <br>
- We can store character constants in character variables and arithmetic operations can be peformed on characters.<br>
 char c ; <br> 
 c = 'A'// in c ,the ASCII code of A which is 65 is stored in binary form <br>
 int d = c + 5 ;// valid statement . d = 70 <br>
 - No operator is assumed to be present. It must be written explicitly. <br>
   a = c.d.b(xy) is not equal to a = c * d * b * ( x * y ) <br>
 - pow() function in math.h

-------------

Rules that are used for the implicit conversion of floating
point and integer values in C, are mentioned below:

- An arithmetic operation between an integer and integer always yields an integer result.
- An operation between a real and real always yields a real result.
- An operation between an integer and real always yields a real result. In this operation the integer is first promoted to a real and then the operation is performed. Hence the result is real.

## TYPE CONVERSION : <br>
 It may so happen that the type of the expression on RHS and the type of the variable on the LHS of an assignment operator may not be same. In such a case, the value of the expression is promoted or demoted depending on the type of the variable on LHS of =.
 -     float a, b, c ;
 -      int s ;
 -      s = a * b * c / 100 + 32 / 4 - 3 * 1.1 ;
  in the assignment statement, some operands are ints whereas others are floats. As we know, during evaluation of the expression, the ints would be promoted to floats and the     result of the expression would be a float. But when this float value is assigned to s it is again demoted to an int and then stored in s.<br>
  
  
## Hierarchy of Operations
While executing an arithmetic statement that has multiple operators, there might be some issues about their evaluation. For example, does 
the expression 2 * x - 3 * y correspond to (2x)-(3y) or to 2(x-3y)? <br>
![image](https://user-images.githubusercontent.com/64036955/119967249-c5a21e80-bfc9-11eb-9b48-d0c4a3a63e9d.png)
Note: if there is any parenthesis in the expressionn, the operation inside the parenthesis is done first. 

Just as for performing mathematical operations, we follow a priority rule, called **BODMS**, here too we follow this priority order to avoid ambiguity.

 ## Associativity of Operators
When an expression contains two operators of equal priority the tie between them is settled using the associativity of the operators. All operators in C have either Left to Right associativity or Right to Left associativity.
 = associates from Right to Left.<br>
 
:diamonds: Control Instruction – This instruction is used to control the sequence of execution of various statements in a C program<br>
There are four types of control instructions in C. They are: <br>
(b) Selection or Decision Control Instruction <br>
(c) Repetition or Loop Control Instruction <br>
(d) Case Control Instruction <br>


   
