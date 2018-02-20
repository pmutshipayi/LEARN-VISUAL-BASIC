## Variable
***
Previously we did create and run our first VB.net application, in this chapter we will talk about variable

Variable:

In computer programming, a variable or scalar is a storage location paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a value.

for example :<br>
   x = 10 <br>
   Then x is a variable

So the question is how to create a variable in visual basic

Syntax :
   ```vbnet
    Dim variable_name as DataType = value
   ```
example :
```vbnet
   Dim x as Integer = 10
```
This is an equivalent of x = 10 in math.<br>
Let come back to our syntax of declaring a variable.

Dim :<br>
  You must note that when you create a variable you must start with the keyword DIM.

*variable_name* :

 There is a set of rules to follow when declaring a variable in visual basic.

 1. Your variable name must start with a letter as first character
 2. The name of variable can't exceed 255 characters in length.
 3. the variable name can't use a space, period ( . ), exclamation mark ( ! ), or the characters @, &;, $, # in the name.
 4. You can declare the same varibale in scope more than one time
 5. And the variable shouldn't use any of the reserved keyword of the programming language.
    for more details about vb.net keyword you can go on https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/keywords/

    Note : vb.net isn't a case-sensitive. that mean when you declare a variable for example called ABC is the same varibale with abc.
    but in case-sensitive programming language such as java, c++ etc. the variable ABC is not abc.

DataType :

a particular kind of data item, as defined by the values it can take, the programming language used, or the operations that can be performed on it.

***List of some data type***

Data type  | value
--------   | -----
Boolean    | False or True
Byte       | 0 through 255 (unsigned)
char       | 0 through 65535 (unsigned)
Date       | 0:00:00 (midnight) on January 1, 0001 through 11:59:59 PM on December 31, 9999
Double     | -1.79769313486231570E+308 through -4.94065645841246544E-324 † for negative values;
Integer    | -2,147,483,648 through 2,147,483,647 (signed)
Object     | Any type can be stored in a variable of type
String     | 0 to approximately 2 billion Unicode characters

for more details : https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/data-types/data-type-summary



**Integer :**

An integer variable can only contain numbers  

__*Valid declaration*__

```vbnet
   Dim x As Integer = 41
   Dim y As Integer = "85522"
```
It's not a must to enclose the value with the *inveted commad* 

__*Invalid declaration*__
```vbnet
Dim age As Integer = "twenty-two"
Dim c As Integer = "hello"
```
Above declaration are invalid, and this will you program to do work properly.

And other thing if you declare a integer as follow
```vbnet
   Dim area As Integer = 74.51
```
The computer will automatically convert *74.51* to *75* because an integer can not be decimal, if you want to declare a variable that will have such values then use a *Double* instead

**Double :**

The *double* data type is also like an *integer* it can only contain numbers, the only defference between the *double* and *integer* is that a *double* can contain decimal numbers while *integer* can't, and a *double* is more bigger than an *integer*

**Boolean :**

A *boolean* value can only be *True* or *False*
example:
```vbnet
Dim adult As Boolean = True
```

**String :**

A *string* value can be anything, any character.

__*Valid declaration*__:
```vbnet
Dim name As String = "Marie, hossane hellena"
```
**Note** : When declaring a *string* variable you must enclose the value with the *inveted commas*

__*Invalid declaration*__:
```vbnet
Dim name As String = Marie, hossane hellena"
``` 

You can declare a variable without giving it a value but you can give it a value later in the program.

Example:
```vbnet
Dim name As String = Nothing
Dim surename As String
Dim age As Integer

name = "Albert"
surename = "Houston"
age = 45
```

Let no create some program that display their values on the screen

Example :
```vbnet
Dim age As Integer = 20
Dim myName As String = "John"        
Dim length As double = 14.20
```

Now let print the result on the screen
```vbnet
Console.WriteLine(age)
Console.WriteLine(myName)
Console.WriteLine(length)
```
And once more do not forget to write the following line :
```vbnet
Console.ReadKey()
```
So the all program will look like this:

```vbnet
Module Module1

    Sub Main()
        Dim age As Integer = 20
        Dim myName As String = "John"     
        Dim length As Double = 14.2
        Console.WriteLine(age)
        Console.WriteLine(myName)
        Console.WriteLine(length)

        Console.ReadKey()
    End Sub
End Module
```
![app](../../img/2.png)


## Comment 
***
In every programming there is a way a programmer can put a comment in his code source.

__*Comment :*__

A comment is a an explain provided in source code by the programmer explainning what the particular code is about.
And then compiling the program the compiler will ignore the comment.

In vb.net to write a comment you must *'* followed by the comment

example:
```vbnet
Dim age As Integer = 41  ' this is our age variable
If age > 18 Then
   ' The user is allow to access the website
End if
```