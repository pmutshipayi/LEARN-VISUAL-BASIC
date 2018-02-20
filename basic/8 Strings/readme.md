## String
---
In computer programming, a string is traditionally a sequence of characters, either as a literal constant or as some kind of variable. The latter may allow its elements to be mutated and the length changed, or it may be fixed (after creation).

In this selection we gonna do some string manipulation.
Earlier we saw how to create a string in this section we will try to a bit deep
```vbnet
Dim message As String = "Hello, world"
Console.WriteLine(message)
```
output :
```
Hello, world
```
__**Uppercase and Lowercase :**__
```vbnet
Console.WriteLine(message.ToUpper)
Console.WriteLine(message.ToLower)
```
output :
```
HELLO, WORLD
hello, world
```
__**Length of the string :**__
Counting the number of character in the string including space
```vbnet
Console.WriteLine(message.Length)
```
output :
```
12
```
__**Replacing character :**__
```vbnet
Console.WriteLine(message.Replace("world", "South africa"))
```
output :
```
Hello, South africa
```
__**Concatenation :**__

In formal language theory and computer programming, string concatenation is the operation of joining character strings end-to-end. For example, the concatenation of "snow" and "ball" is "snowball".

```vbnet
Dim message As String = "Hello, world"
message += "I really happy to have you guys here "
message += "Hope you are doing well"
Console.WriteLine(message)
```
output :
```
Hello, worldI really happy to have you guys here Hope you are doing well
```
As you have noticed the output everything is in one line, but you can break them into lines using.
```
vbNewLine
```
Let illustrate it with an example
```vbnet
Dim message As String = "Hello, world" & vbNewLine
message += "I really happy to have you guys here" & vbNewLine
message += "Hope you are doing well" & vbNewLine

Console.WriteLine(message)
```
output :
```
Hello, world
I really happy to have you guys here
Hope you are doing well
```
__**Contains :**__

Checking if the string contains a specific string
```vbnet
Dim message As String = "Hello, world"
Console.WriteLine(message.Contains("love"))
Console.WriteLine(message.Contains("world"))
```
output :
```
False 
True
```
__**Start with and End with :**__

Check if the string start or end with a specific string.
```vbnet
Dim message As String = "Hello, world"

Console.WriteLine(message.StartsWith("me"))
Console.WriteLine(message.EndsWith("world"))
```
output :
```
False
True
```
__**Split :**__

The split() method splits a String object into an array of strings by separating the string into substrings, using a specified separator string to determine where to make each split.
```vbnet
 Dim message As String = "Hello, world"
'split the string where ever there is a comma 
Dim splited() As String = message.Split(",")
'Loop the array
For i As Integer = 0 To splited.Length - 1
    Console.WriteLine("Index " & i & " is " & splited(i))
Next
```
output :
```
Index 0 is Hello
Index 1 is  world
```
Example :

A program that count the number words containing in a sentence
```vbnet
Module Module1
    Sub Main()
        Console.Write("Enter a sentence : ")
        Dim sentence As String = Console.ReadLine()
        'Split the sentence by space separator
        Dim sp() As String = sentence.Split(" ")
        Console.WriteLine("Your sentence contains " & sp.Length & " word(s)")
    End Sub
End Module
```
output :
```
Enter a sentence : God is good and great
Your sentence contains 5 word(s)
```