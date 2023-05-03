# [C Language](https://en.wikipedia.org/wiki/C_(programming_language))

# Pointers

```C
/******************************************************************************

                            Online C Compiler.
                Code, Compile, Run and Debug C program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <stdio.h>

int main()
{
    int     a_int;  
    float   a_float;
    
    int*    a_int_p;    
    float*  a_float_p;  
    
    void*   a_void_p = 0;
    
    printf("----------------------------------------------------------------\n");
    a_int   = 5;
    a_int_p = &a_int;
    printf("The Value        of `a_int`             variable is: %d\n", a_int);
    printf("The Adress       of `a_int`             variable is: %p\n", &a_int);
    printf("The Value        of `a_float`           variable is: %f\n", a_float);
    printf("The Adress       of `a_float`           variable is: %p\n", &a_float);

    printf("----------------------------------------------------------------\n");
    a_int   = 5;
    a_int_p = &a_int;
    printf("The Value stored at `a_int_p`   pointer variable is: %d\n", *a_int_p);
    printf("The Value        of `a_int_p`   pointer variable is: %p\n", a_int_p);
    
    printf("----------------------------------------------------------------\n");
    a_float = 2.7;
    a_float_p = &a_float;
    printf("The Value stored at `a_float_p` pointer variable is: %f\n", *a_float_p);
    printf("The Value        of `a_float_p` pointer variable is: %p\n", a_float_p);

    printf("----------------------------------------------------------------\n");
    a_void_p = &a_int;
    *((int*)a_void_p) = 10;
    printf("The Value stored at `a_void_p`   pointer variable is: %d\n", *((int*)a_void_p));
    printf("The Value        of `a_void_p`   pointer variable is: %p\n", a_void_p);
    
    printf("----------------------------------------------------------------\n");
    a_void_p = &a_float;
    *((float*)a_void_p) = 27.0;
    printf("The Value stored at `a_void_p`   pointer variable is: %f\n", *((float*)a_void_p));
    printf("The Value        of `a_void_p`   pointer variable is: %p\n", a_void_p);

    printf("----------------------------------------------------------------\n");
    a_int   = 5;
    a_int_p = &a_int;
    printf("The Value        of `a_int`             variable is: %d\n", a_int);
    printf("The Adress       of `a_int`             variable is: %p\n", &a_int);
    printf("The Value        of `a_float`           variable is: %f\n", a_float);
    printf("The Adress       of `a_float`           variable is: %p\n", &a_float);
    
    return 0;
}


```