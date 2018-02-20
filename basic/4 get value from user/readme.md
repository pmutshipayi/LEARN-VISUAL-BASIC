## Get value from user
***
In this section we'll see how to get any value from the user and the store it a variable.

```vbnet
Console.Write("Hey, what is your name : ")
Dim name As String = Console.ReadLine()
Console.Write("Welcome ")
Console.Write(name)
Console.ReadKey()
```
Done. the run the application

**Explanation**
```vbnet
Console.Write()
```
When write the above line, it's will simply write something on the screen
```vbnet
Console.WriteLine()
```
The above line write a new line to the Console unlike *Console.Write()* that write something on the screen without creating a new line.

```vbnet
  Console.ReadLine()
```
The above code read a line from the user
```vbnet
  Console.ReadKey()
```
The above code read a key from the user example 4, a, etc.


So finally let put all of them in one and run our program
```vbnet
Module Module1
    Sub Main()
        Console.Write("Hey, what is your name : ")
        Dim name As String = Console.ReadLine()
        Console.Write("Welcome ")
        Console.Write(name)
        Console.ReadKey()
    End Sub
End Module
```
output :

![output](../../img/4.png)
