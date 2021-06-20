## Pointers
 Pointers are **address variables** , which means these store the address of variables .
 
 #### Variable is a named memory location.
  **int i =5;**  This declaration gives us the following information:<br>
       ![snip variable](https://user-images.githubusercontent.com/72215893/121034311-8c885c00-c7ca-11eb-87e9-5db0f7a0b8bd.png)
  We can print the adress of our variable in this way:
            
               printf ( "Address of i = %u\n", &i ) ; // 65524
               printf( "value of i = %u \n", i);  // 5
               printf ( "Value of i = %d\n", *( &i ) ) ;
  
 #### Here **&** is address of operator.It gives the adress of the variable<br>
 #### Here * is called ‘value at address’ operator. It gives the value stored at a particular address. The ‘value at address’ operator is also called ‘indirection’ operator
 ###### %u is a format specifier to print address of any variable.
 ####  printing the value of *( &i ) is same as printing the value of i.
 
 If we store the address of i in some variable like  <br>
             
             int j = &i; // this is pointer
             printf("Address of j %u ", &j ) ; // adress of j
              printf("value of i %d %d %d ", i , *j, *(&)i );
             
 ![pointer](https://user-images.githubusercontent.com/72215893/121064824-ac794900-c7e5-11eb-9b63-ef5a79c42ccb.png)
   ##### we can’t use j in a program without declaring it , so we need to declare it .
              int *j ;
              j = &i; // in this statement , we are telling the compiler that j is storing the address of i
              
 - This is how we declare a pointer. ( with an asterick symbol)
- This declaration tells the compiler that j will be used to store the address of an integer value
-------------------------------------------------------------------------------------------------------------
##### Pointers are variables that contain addresses, and since addresses are always whole numbers, pointers would always contain whole numbers .
int *alpha ;    char *ch ;    float *s ;  **in all the three declarations , s is always going to store whole numbers and the value aof the pointed location can be anything**

#### Pointer to Pointer 
 
 ![_Let us C pdf - Personal - Microsoft​ Edge 07-06-2021 11_28_15 PM](https://user-images.githubusercontent.com/72215893/121067080-3fb37e00-c7e8-11eb-9c36-6d2ba8319f92.png)
 
 A pointer can also point to another pointer
 
           int i =  3;
           int *j = &i;
           int **k = &j; // pointer to pointer
            printf("Value of i %d %d %d" , i , *j ,**k);
            printf ( "Address of j = %u\n ", k , &j) ;
            printf ( "Address of i = %u\n", &i ,j ) 
            
            
   ## Parameter passing techniques
   
   ### 1 . Call By Value
   
 ##### In call by value a copy of actual arguments is passed to respective formal arguments.
 ##### any change made to the formal arguments in the called function have no effect on the values of actual arguments in the calling function. Changes done to formal parameter do not reflect back to actual parameters
            
           # include <stdio.h> 
            void swapv ( int x, int y ) ;
            int main( )
            {
             int a = 10, b = 20 ;
             swapv ( a, b ) ;
             printf ( "a = %d b = %d\n", a, b ) ;
             return 0 ;
            }
            void swapv ( int x, int y ) 
           {
            int t ;
            t = x ;
            x = y ;
            y = t ;
           printf ( "x = %d y = %d\n", x, y ) ;
            }

  
   
   
   ### 2. Call By Address
  ##### In call by address, the location (address) of actual arguments is passed to formal arguments/parameters.
  ##### Any changes to the formal parameter are reflected in the actual parameter in the calling environment as formal parameter receives a reference (or pointer) to the actual    data. (using these addresses, we would have an access to the actual arguments ).
  
          void swapA ( int *x, int *y )
          {
           int t ;
           t = *x ;
           *x = *y ;
           *y = t ;
          }
   
   ###### Using a call by reference intelligently, we can make a function return more than one value at a time, which is not possible ordinarily. 
       
        # include <stdio.h>
        void areaperi ( int, float *, float * ) ;
        int main( )
      {
       int radius ;
       float area, perimeter ;
       printf ( "Enter radius of a circle " ) ;
       scanf ( "%d", &radius ) ;
       areaperi ( radius, &area, &perimeter ) ;
       printf ( "Area = %f\n", area ) ;
       printf ( "Perimeter = %f\n", perimeter ) ;
       return 0 ;
     }
     void areaperi ( int r, float *a, float *p )
      {
     *a = 3.14 * r * r ;
     *p = 2 * 3.14 * r ;
      }


 ### 3. Call By Reference
 A reference is an alias to an existing variable
     
     int a=5;
     int &ref = a; 
     
 ##### Any changes to the formal parameter are reflected in the actual parameter .
 ##### In call by reference, the location (address) of actual arguments is passed to formal arguments/parameters.
 
 
         
         #include <stdio.h>
         void swapr(int&a, int& b); 
         int main() 
        {
         int n1 = 10, n2 = 20;
         swapr(n1, n2);
         printf("n1: %d, n2: %d\n", n1, n2);
         }
 
        void swapr(int& a, int& b)
        {
         int t;
         t = a; a = b; b = t;
         }
