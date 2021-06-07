In real life, we are often faced with situations where we are required to make a choice between a number of alternatives rather than only one or two.<br>
For example, which school to join or which hotel to visit, or still harder, which girl to marry. <br>
Serious C programming is same; the choice  Sometimes we are asked to make is more complicated than merely selecting between two alternatives<br>

### Switch-Case Statement<br>
The control statement that allows us to make a decision from the number of choices is called a switch -case statement.<br>

#### Syntax

      switch ( expression )
      {
       case constant 1 :
          do this ;
      case constant 2 :
          do this ;
      case constant 3 :
          do this ;
      default :
          do this ;
      }
      
-  If suppose case 1 matches with the expressin inside switch , Then all the statements under case 2 , case 3 and default will be esxecuted . This is not what we expected . So to teerminate the execution after case 1 
-  We use **break statement**. This situation is called as fall through.( which means falling through the entire switch )

         int i = 2 ;
        switch ( i ) 
       {
       case 1 :
        printf ( "I am in case 1 \n" ) ; 
        break ;
       case 2 :
         printf ( "I am in case 2 \n" ) ; 
         break ;
       case 3 :
         printf ( "I am in case 3 \n" ) ; 
         break ;
       default :
          printf ( "I am in default \n" ) ; 
      }

       output//( in presence of break statement) I am in case 2
       output//(in presence of break statement)I am in case 2 
                                               I am in case 3
                                                I am default
                                                
  ### NOTE:
  - We can use any variable or exprssion in switch condition.
  - We can execute a common set of statements for multiple cases.
  - Even if there are multiple statements to be executed in each case, there is no need to enclose them within a pair of braces (unlike ifand else). 
  - Every statement in a switch must belong to some case or the other.If a statement doesn’t belong to any case, the compiler won’t report an error.
  
        switch ( i )
        {
         printf ( "Hello\n" ) ;
         case 1 :
            j = 10 ;
              break ;
        case 2 :
         j = 20 ;
          break ;
        }
         //  the compiler will never print hello
         
    - Switch case is a **single expression equality check** statement . It is a good replacement of if else statement when we are performing some equality checks.
    -  We can check the value of any expression in a switch.( expressions containing only constants ,not variables) . 
    
            switch ( i + j * k )
           switch ( 23 + 45 % 4 * k )
            switch ( a < 4 && b > 7 )
    - The break statement when used in a switch takes the control outside the switch. However, use of continue will not take the control to the beginning of switch as one is likely to believe. This is 
     because switch is not a looping statement unlike while, for or do-while .
    - In principle, a switch may occur within another, but in practice, a nested switch  is rarely done 
    - A float expression cannot be tested using a switch.
    - Multiple cases cannot use same expressions;
    
           switch(a)
          { case 2:
            
            case 1+1:  // illegal
         }

### if-else vs switch
switch works faster than an equivalent if-else ladder. How come? This is because the compiler generates a jump table for a switch during compilation. As a result, during execution it simply refers the jump table 
to decide which case should be executed, rather than actually checking which case is satisfied. As against this, if-elses are slower because the conditions in them are evaluated at execution time<br>

### GOTO statement
goto is a jump statement. we can trasfer the control of the program to anywhere with goto. But in real programming , using goto is a really bad practice.<br>

 ##### SYNTAX
      
       goto label ;
       
       label:
       
  - Any number of gotos can take the control to the same label.
  - The only programming situation in favour of using goto is when we want to take the control out of the loop that is contained in several other loops.

         int main( )
         {
        int goals ;
        printf ( "Enter the number of goals scored against India" ) ;
        scanf ( "%d", &goals ) ;
        if ( goals <= 5 )
            goto sos ;
        else
        {
          printf ( "About time soccer players learnt C\n" ) ;
            printf ( "and said goodbye! adieu! to soccer\n" ) ;
         exit ( 1 ) ; /* terminates program execution */
         }
         sos :
        printf ( "To err is human!\n" ) ;
        
       }  
