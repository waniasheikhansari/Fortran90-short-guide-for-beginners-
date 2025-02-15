# Introduction to Fortran 90

It is a high level programming language used to handle large datasets in physics, mathematics also used in numerical simulations. 

## Basic Hello world program:
- First keyword in every program must always be `program` followed by program name.
- To display output in fortran use keyword, ` print *, `
- Lastly keyword `end` to end the program. 
- Note: fortran is case insensitive language. 

#### Example:

```fortran
Program HelloWorld
    Print *, "Hello, World!"
end
```
# Data Types:
It has 5 fundamental data types.
1. Integers: they store whole numbers
2. Real: they store floats
3. Complex: stores complex
4. Character: stores strings
5. Logical: stores boolean values
## Integers:
- Any number with no decimal point stores in this data type.
- Numbers can be positive, Negative, or zero.
#### Example: 
```
program integer_example
    implicit none
    integer :: a, b, sum
    
    a = 10
    b = 20
    sum = a + b
    
    print *, "Sum:", sum
end
```
# Real:
- Any float number i.e number with decimal value stores in this data type
#### Example:
```
program real_example
    implicit none
    real :: x, y, product
    
    x = 3.14
    y = 2.5
    product = x * y
    
    print *, "Product:", product
end
```
# Complex
- Allows stroage of complexs in the format z(x+iy)
  where, z can be any varriable representing complex, x is the real part, and y is the imaginary part
#### Example:
```
program complex_example
    implicit none
    complex :: z1, z2, zsum
    
    z1 = (3.0, 4.0)   ! 3 + 4i
    z2 = (1.0, -2.0)  ! 1 - 2i
    zsum = z1 + z2
    
    print *, "Sum of Complex Numbers:", zsum
end
```
# Character:
- The CHARACTER data type in Fortran can store special characters, including symbols like @, #, $, %, &, *, and even whitespace, punctuation, and escape sequences.
- Note: In Fortran, you need to declare lenght(len) of string in CHARACTER variable, because Fortran does not automatically allocate memory for character string
#### Example: 
```
program character_example
    implicit none
    character(len=10) :: name
    name = "Wania"
    
    print *, "Name:", name
end
```
# Logical:
- It is typically used in conditional statements, loops, and logical operations.
### Fortran Logical Operators

Fortran supports logical operations using the following operators:

| **Operator** | **Description**               | **Example**                  |
|-------------|--------------------------------|------------------------------|
| `.NOT.`     | Logical NOT (negation)        | `.NOT. .TRUE.` → `.FALSE.`   |
| `.AND.`     | Logical AND (conjunction)     | `.TRUE. .AND. .FALSE.` → `.FALSE.` |
| `.OR.`      | Logical OR (disjunction)      | `.TRUE. .OR. .FALSE.` → `.TRUE.`   |
| `.EQV.`     | Logical equivalence           | `.TRUE. .EQV. .TRUE.` → `.TRUE.`   |
| `.NEQV.`    | Logical non-equivalence       | `.TRUE. .NEQV. .FALSE.` → `.TRUE.` |


#### Example
```
program logical_operator
    implicit none 
    logical :: a,b,res1, res2
    a = .TRUE.
    b= .FALSE.
    res1= a .AND. b
    res2= a .OR. b 
    
    print*, " A AND B ", res1
    print*, "A OR B ", res2
end
```


