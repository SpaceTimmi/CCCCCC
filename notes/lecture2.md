Variables and datatypes:
    The C programming language is a weakly typed language. 

    Some C datatypes:
    * Numeric (int, float, double)
    * Character (char)
    * User defined (struct, union)

    More on numeric datatypes:
    Depending on precision and range required, one of the following can be used.
              |           SIGNED     |  UNSIGNED 
    * short   | ``` short int x; ``` | ```unsigned short int x; ```    |
    * default | ``` int x;       ``` |
    * long    | ``` long x;      ``` |
    * float   | ``` float x;     ``` |  NA
    * double  | ``` double x;    ``` |  NA
    * char    | ``` char x;      ``` |

    Unsigned versions have rougly double the range of signed.
    Signed and unsigned only differs in arthimetic expressions.
    Sizes are complier machine/dependent, but roughly the  
       sizeof(char) < sizeof(short) <= sizeof(long) and
       sizeof(char) < sizeof(short) <= sizeof(float) <= sizeof(double)  

    Note: Big Endian and Little Endian orders.
    Big Endian: The "most" significant bits occupy the lower address. Networks generally use the big endian order.
    Little Endian: The "least" significant bits occupy the lower address. This representation is used on all x86 compatible processors.

    Constants are literal/fixed values assigned to variables or used directly in expressions.
    Format for declarations in C: type variable-name[=value]
      examples: char x; uninitialized
                char x= 'A'; intialized to A.
                char x=y= 'Z'; multiple initializations to Z.

    Bitwise operators:
    * &  (AND) true if "both" operands are true.
    * |  (OR)  true if "any" operand is true.
    * ^  (XOR) true if "only one" operand is true.
    * << (left shift)
    * >> (right shift)


Conditonal Expressions:
  if(cond)
      x=<expra>
  else
      x=<expra>
  Note: ternary operator usesage is the same as in JavaScript.



