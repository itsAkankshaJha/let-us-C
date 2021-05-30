# let-us-C
we humans communicate with each other with a certain medium ,wihch is the language we speak<br>
Similarily, How do you think we communicate with a computer?<br>
A computer has its own set of instructions what we call computer language<br>
1. low level language -
 Machine language- language of 0 and 1 ,  understandable by the machine ,basically interacts with the hardware <br>
 Assembly language - Assembly language uses a mnemonic to represent each low-level machine instruction or opcode//instead of 0&1 we use english words ,names and symbols <br>
Assembly code is converted into executable machine code by a utility program referred to as an assembler.
2. High level language - lang like C,C++,JAVA etc<br>
-----------------------------------------------------------------------------------------------------------------

#### Origin of C:
It was developed at Bell Labs, by Dennis Ritchie, Ken Thompson and others. It was a by-product of the UNIX operating system. Like other operating systems of that time, UNIX was written in assembly level language. </br>
programs written in assembly level language are hard to debug and enhance, and UNIX wwas no exception.
Ken Thompson then decided that a higher level language was needed for further development of UNIX , so he designed a language named "B".</br>

Soon, Dennis Ritchie joined the UNIX project and started programming in B. In 1970, Bell Labs acquired  a PDP 11 for the UNIX project. Once unix was up and running on PDP 11, Thompson, rewrote a portion of UNIX in B.
and it became apparent that B wasn't well suited for PDP 11, So Ritchie began to develop an "extended version of B". He named it as NB at first, nbut upon more developments, when it diverted more from B, name was changed to "C". </br>
By 1973, the language was stable enough that UNIX could be written in C.
It provided an important benifit : **portability**.  By writing compilers in C for other computers at Bell Labs, it couldb be used on other machines as well!

#### Standardization:
C continued to involved during the 1970 specially between 1977 and 1979.Iit was during this period the first book of C appeared, “ the C programming language” by Brian kernighan and Dennis Ritchie which was published in 1978 but in the absence of this official standard book for C this book known as the K & R or the “white book “, served as a standard reference.
 During 1977, relatively few C programs and most of them were UNIX users. By the 1980s, however, C expanded beyond the narrow confines of the Unix world. C compilers became available on a variety of Machines, running a different operating system. In particular, C began to establish itself on the fast-growing IBM PC platform . </br>

Programmers who wrote new C compilers relied on K and R as a reference. Unfortunately it was not clear about many of the features and it did not have a clear distinction which features belong to C and which were a part of Unix. Also, C continued to change after K&R  was published, with new features being added and a few older ones being removed. Need of a thorough, precise and up-to-date description of the language soon became Apparent.  Without such a standard numerous dialects would have ryzen 13 the portability of the C programs.
The development of US standard for C began in 1983, under the auspices of the ANSI. After many revisions, the standard was completed in 1988 and formally approved in December 1989 as ANSI standard. In 1998, it  was approved by international organisation for standardization (ISO).
This is reffered to as the *C89 version.

-------------------

Four important aspects of any programming language:/<br>
how it stores data <br>
how it operates on data<br>
how the exact sequence of instruction works<br>
input and output methods <br>

C language is simple,reliable and easy to use and it has survived for more than three decades in an industry wheren newer languages and technologies emerge and vanish day in and day out .<br>
Why learn C :eyeglasses: when we have C++,Java,Python in trend?<br>
:sunglasses: In order to be good with programming ,one should have a good hold over C as it is reliable ,simple and basic.So it makes more sense to first learn C and then migrate to C++, C# and Java. Though this two-step learning process may take more time,but at the end of it you will definitely find it worth the trouble.<br>

:sunglasses:  major parts of popular OS like UNIX,LINUX and Android is written in C .And when it comes to performance (speed of execution) nothing beats C.<br>
:sunglasses: The devices we use like oven ,microwave,washing machines ,cameras ,their microprocessors,os and embedded system are written in C programs run fast .<br>
:sunglasses:  GAME DEVELOPMENT :  Many popular gaming frameworks (like DirectX) have been built using C due its high execution speed .<br>


# LEARNING C , LET'S BEGIN :computer:<br>
when we start learning english in our childhood ,we always start from learning alphabets ,then words ,then we from sentences ,sentences to form paragraphs<br>
Similarily in C :<br> 
Alphabets(A-Z,a-z),special symbols,numbers(0-9) :point_right: reserve words/constants/identifiers :point_right: instructions :point_right: program/code<br>
 **Constants,reserve words and variables<br>**
 . A constant is an entity that doesn’t change: two types : primary and secondary constants <br>
 In PRIMARY constants ,we have integer contant(no commas,blank spaces ,no decimal points,no other symbols) <br>
 ### real constant <br>
   :nerd_face::nerd_face: when the real number is so too large ,it can be expressed in exponential form : mantissa and exponent part(-3.4e38 to 3.4e38) e or E <br>
   Rules for creating a Float constant:
* The mantissa part and the exponential part should be separated by a letter e or E.
* The mantissa part may have a positive or negative sign. 
* Default sign of mantissa part is positive. 
* The exponent must have at least one digit, which must be a positive or negative integer. Default sign is positive.

   
 character constant: a single alphabet, a single digit or a single special symbol enclosed within single inverted commas.('A' , '6') <br>
 
 
 C VARIABLES : rules of naming to be followed(max length of var can be 247 :dizzy_face: ,but we make shorter and meaningful names)<br>
  KEYWORDS : 32 <br>
  
 :hugs: FIRST C PROGRAM :hugs: <br>
  :ghost: COMMENTS ( / * ...... * /):ghost:<br>
:technologist: **MAIN()** <br>
  Variable declaration and usage <br>
  :cherry_blossom: PRINTF() - it can print variables ,expressions and constants<br>
   :maple_leaf: SCANF() - to input variables<br>
   **COMPILATION AND EXECUTION OF CODE**<br>
   
   -----------------------------------------------------------------------------------------------------------------------------------
   
