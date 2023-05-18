# The DummyDimension Language
Hello. 
This is a programming language. It's more like a sequence of controlling a virtual object, but whatever.

# Dimension

A dimension (in this language) is one dimension array, that consists of _powers of specified radix._
Radix is specified by the first number that is provided in a line. For example, the code that creates an object and a dimension, which has the radix of 2, would be : 

```
2 [object control code here]
```

And to visualize the values of each elements of dimension, it would be :  

```
      +- -3 -+- -2 -+- -1 -+- 0 -+- 1 -+- 2 -+- 3 -+- 4 -+- 5 -+- 6 -+- 7 -+- 8 -+
...   |  1/8 |  1/4 |  1/2 |  1  |  2  |  4  |  8  | 16  |  32 |  64 | 128 | 256 | ... 
      +------+------+------+-----+-----+-----+-----+-----+-----+-----+-----+-----+

```

You can create many objects as you want, and many dimension for them. _Note that there also exists negative exponent, and negative radix._
The object starts at the offset 0, which consists the value of 1.

# Object

Each line of the code is one object that exists in a dimension, as previously shown. An object can consists of value.
An object does what object control code commands, which can be getting the value from dimension, or setting the array of the dimension to value it consists.

The object control code is constructed by each character. One character provides one movement of the object. The object moves along the dimension horizontally, 
and one object cannot move between dimension. 

You can create more than one object, and those objects can exist in same dimension. For example, this is a code that creates two object that exists in same dimension : 
```
2 [object 0 control code here]
2 [object 1 control code here]
```
This code would create two object that starts in index 0, that are in same dimension.

```
                          Obj0 Obj1
                            V   V
      +- -3 -+- -2 -+- -1 -+- 0 -+- 1 -+- 2 -+- 3 -+- 4 -+- 5 -+- 6 -+- 7 -+- 8 -+
...   |  1/8 |  1/4 |  1/2 |  1  |  2  |  4  |  8  | 16  |  32 |  64 | 128 | 256 | ... 
      +------+------+------+-----+-----+-----+-----+-----+-----+-----+-----+-----+

```
Each objects have its specified index, which corresponds to the number of line that the code of object exists. 
(As shown previously, the object 0 would be in line 1 and object 1 would be in line 2.)

# Movement and Instructions of Object

After the specified dimension radix, we provide the movement of the object : 
1. Right    : Move object to right (Increase index)
2. Left     : Move object to left  (Decrease index)
3. Add      : Add the value of current array of dimension to the value of object
4. Subtract : Subtract the value of current array of dimension from the value of object
5. Move     : Move the value of current array of dimension to the value of object
6. Print    : Print the value of the object (In style of ascii)
7. Throw    : Set the value of object to zero

The object control code is the first characters of these instructions, which is : 
1. Right    -> R
2. Left     -> L
3. Add      -> A
4. Subtract -> S
5. Multiply -> X
6. Move     -> M
7. Print    -> P
8. Throw    -> T

_A number is not considered as one character. The whole number will be considered as one instruction._

For example, the code that moves object to right three times would be : 

```
2 RRR
```

# Instruction that has parameter
The fundamental syntax of instructions that consist parameter is : 
```
[Instruction character][number of object, or other parameter]
```
The instruction characters and its function are : 
1. Add       -> A\[Object number\] : Add the value of specified object to the value of current object
2. Subtract  -> S\[Object number\] : Subtract the value of specified object from the value of current object
3. Set Flag  -> F\[Flag number\] : Set flag to the current point. You can go back to this point by using Jump instruction
4. Jump to   -> J\[Flag number\] : Jump to the specified flag, **when the lastest result of calculation is zero**

# Spacing the instructions

later
