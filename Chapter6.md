### The for loop 
This is the most popular looping instruction.<br>
The for allows us to specify **three things** about a loop in a single line: <br>
- **initialisation ,  condtion and variation of counter**

Syntax:

    for ( initialize counter ; test counter ; variation of counter )
    {
     do this ;
     and this ; 
     and this ;
   }
   
 ### NOTE :
   - If there is only one statement in the body of the for loop, the pair of braces can be dropped.
   - if we have skipped incrementation or declaration of variable ,still we have to put semicolons.
   
          for(int i=0; i<5; )
         {  printf("HELLO");
          i=i+1;
         }
         
          
          int i=9;
           for( ; i<5 ; )
         {  printf("HELLO");
          i=i+1;
         }
   - comparison as well as the incrementation can be  done through the same expression.
   
          int i=0;
          for( ; i++< 10 ; )
         {  printf("HELLO"); // firstly incrementation is done, followed by comparison
         
         }
         
  - The way if statements can be nested, similarly **while** and **for** can also be **nested**.    
         
          for( int i=0 ; i< 10 ; i++)
          { for(int j=0; j<5; j++)
             statements ;
          }
       
   - In for loop ,there can be multiple initialization, variations but there will be only **one condition** 
   
            for( int i=0; int j=0; i<10 ; i++; j--) 
               {   statements ;
               }
               
   ### The break Statement
   We often come across situations where we want to jump out of a loop instantly, without waiting to get back to the condition. The keyword **break** allows us to do this. <br>
   **Q :** Check if a number is prime or not using break statement.<br>
   
   ### The continue Statement
   In some programming situations, we want to take the control to the beginning of the loop, bypassing the statements inside the loop, which have not yet been executed. The      keyword **continue** allows us to do this. 
   
     for ( i = 1 ; i <= 2 ; i++ )
    {
     for ( j = 1 ; j <= 2 ; j++ )
     {
      if ( i == j )
      continue ;
       else if( i%2==0)
         break;
     printf ( "%d %d\n", i, j ) ;
    }
  }

### The do-while Loop
     
     do
    {
      this ;
     and this ;
    } while ( this condition is true ) 
    
-  There is a minor difference between the working of while and do-while loops. This difference is the place where the condition is tested. The **while**tests the condition before executing any of the statements within its loop. But the **do-while**tests the condition after having executed the statements within the loop.<br>   
-  do-while would execute its statements at least once, even if the condition fails for the first time. The while, on the other hand will not execute its statements if the condition fails for the first time.


        #include <stdio.h>
         int main( )
        {
         char another ;
         int num ;
        do
       {
       printf ( "Enter a number " ) ;
       scanf ( "%d", &num ) ;
        printf ( "square of %d is %d\n", num, num * num ) ;
       printf ( "Want to enter another number y/n " ) ;
       fflush ( stdin ) ;
        scanf ( "%c", &another ) ;
       } while ( another == 'y' ) ;
       return 0 ; // e do-while loop would keep getting executed till the user continues to answer y.
      }
      
      #### fflush(stdin)
      It is designed to remove or **‘flush out’** any data remaining in the buffer. The argument to fflush( ) must be the buffer which we want to flush out. Here we have used **‘stdin’** , which means buffer related with standard input device, i.e., keyboard.<br> 
After supplying a number when we hit the Enter key, scanf( ) assigns the number to variable num and keeps the Enter key unread in the keyboard buffer. So when it’s time to supply Y or N for the question ‘Want to enter another number (y/n)’, scanf( ) will read the Enter key from the buffer thinking that user has entered the Enter key. To avoid this problem, we use the function fflush( ). I
