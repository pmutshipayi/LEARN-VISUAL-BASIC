## Functions
---
In programming, a named section of a program that performs a specific task. In this sense, a function is a type of procedure or routine. Some programming languages make a distinction between a function, which returns a value, and a procedure, which performs some operation but does not return a value.

In vbnet there are two types of function,a function that return a value and the other one that does not return any value.

*Function that return a value :*

Syntax :
```
Function name_of_the_function() As DataType
    Return value
End Function
``` 
Example :
```vbnet
Function x() As Integer
    Return 10
End Function
```
**Note :** when naming a function you must follow those rules of naming a variable

*Function that does not return a value:*

Syntax:
```
Sub name_of_the_function()
    code to execute
End Sub
```
Example :
```vbnet
Sub x()
    'Code goes here
End Sub
```
*Calling a function :*

After declaring a function i can call that function whenever i want and as many times as i want.

example:
```vbnet
Module Module1
    Sub Main()
       'Call a the function getName()
       getName()
    End Sub
    ' create the function getName()
    Function getName() As String
        Return "Pascal"
    End Function
End Module
```
One more 
```vbnet
Module Module1
    Sub Main()
       'Call a the function getName() and put it in the variable name
       Dim name As String = getName()
       Console.WriteLine(name)
    End Sub
    ' create the function getName()
    Function getName() As String
        Return "Pascal"
    End Function
End Module
```
output :
```
Pascal
```
A function that ask the user his name then return the name
```vbnet
Module Module1
    Sub Main()
       'Call a the function askUserName
        Console.WriteLine("Your name is " & askUserName())
        Console.ReadKey()
    End Sub
    Function askUserName() As String
        Console.Write("Hello, what's your name : ")
        Return Console.ReadLine()
    End Function
End Module
```
output :
```
Hello, what's your name : parfait
Your name is parfait
```
Try the same using now a sub procedure 
```vbnet
Module Module1
    Sub Main()
        'Call a the function askUserName
        askUserName()
    End Sub
    Sub askUserName()
        Console.Write("Hello, what's your name : ")
        ' As with a sub we can't return any value, so let display right away
        Console.WriteLine("Your name is " & Console.ReadLine())
    End Sub
End Module
```
output :
```
Hello, what's your name : parfait
Your name is parfait
```
A function return anything even an array or list, let create a function that ask the user five names and then stores those names in an ArrayList then return the list
```vbnet
Module Module1
    Sub Main()
       'Call a the function askUserName
        Dim names As List(Of String) = askUserName()
        'Display those names
        For Each name As String In names
            Console.WriteLine(name)
        Next
    End Sub
End Module
Function askUserName() As List(Of String)
   Dim names As New List(Of String)
    For i As Integer = 0 To 4
        Console.Write("Enter any name : ")
        names.Add(Console.ReadLine())
    Next
    Return names
End Function
```
output :
```
Enter any name : parfait
Enter any name : John
Enter any name : Peter
Enter any name : Thomas
Enter any name : Helene
parfait
John
Peter
Thomas
Helene
```
__**Functions with parameter :**__

You can parse an argument (parameter) in your function

Syntax :
```
Function name_of_the_function(byval param As DataType, ...)As DataType
    code to execute
End Function

Sub function_name(byval param As DataType, ...)
    code to execute
Sub
```
examples :
```vb
Function getAgeFromYearOfBorn(Byval yearOfBorn As Integer) As Integer
    Dim d As Date = Date.Today
    return d.Year - yearOfBorn
End Function
'Try with a sub
Sub addition(Byval a As Integer, Byval b As Integer)
   Dim sum As Integer = a + b
End Sub  
```
Let make it complete
```vb
Module Module1
    Sub Main()
        ' Call getAgeFromYearOfBorn
        Dim age As Integer = getAgeFromYearOfBorn(1991)
        Console.WriteLine("Age : " & age)
        ' Do the addition of two numbers
        addition(57, 100)
    End Sub
    Function getAgeFromYearOfBorn(ByVal yearOfBorn As Integer) As Integer
        Dim d As Date = Date.Today
        Return d.Year - yearOfBorn
    End Function
    'Try with a sub
    Sub addition(ByVal a As Integer, ByVal b As Integer)
        Dim sum As Integer = a + b
        Console.WriteLine(a & " + " & b & " = " & sum)
    End Sub
End Module
```
output :
```
Age : 27
57 + 100 = 157
```