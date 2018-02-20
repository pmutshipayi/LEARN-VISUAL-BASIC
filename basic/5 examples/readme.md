## Examples
***
The do some exercises for everything we have seen earlier.

1.Write a Hello, world program

```vbnet
Module Module1
   Sub Main()
     Console.Write("Hello, world")
     Console.ReadKey()
  End Sub
End Module
```

2.A program that ask the user name an display it on the screen
```vbnet
Module Module1
    Sub Main()
        Console.Write("What is your name : ")
        Dim name As String = Console.ReadLine()
        Console.Write("Welcome ")
        Console.Write(name)
        Console.ReadKey()
    End Sub
End Module
```

3.A program that find the sum of the variables, and the display the result on the screen.
```vbnet
Module Module1
    Sub Main()
        Dim x As Integer = 45
        Dim y As Integer = 10
        Dim z As Integer = x + y
        Console.WriteLine(z)
        Console.ReadKey()
    End Sub
End Module
```

4.A program that check the biggest value between X and Y
```vbnet
Module Module1
    Sub Main()
        Dim x As Integer = 45
        Dim y As Integer = 10
        If x > y Then
            Console.WriteLine("X is greater than Y")
        Else
            Console.WriteLine("Y is greater than X")
        End If
        Console.ReadKey()
    End Sub
End Module
```

5.A program that check if A is equal to B and C greater than A
```vbnet
Module Module1
    Sub Main()
        Dim a As Integer = 45
        Dim b As Integer = 10
        Dim c As Integer = 30
        If a = b And c < a Then
            Console.WriteLine("Condition success")
        Else
            Console.WriteLine("Condition evaluation return a false")
        End If
        Console.ReadKey()
    End Sub
End Module
```

6.Operation program
```vbnet
 Module Module1
    Sub Main()
        Dim a As Integer = 45
        Dim b As Integer = 10
        Dim c As Integer = 30

        Console.WriteLine("a * b = " & a * b)
        Console.WriteLine("a * b * c = " & a * b * c)
        Console.WriteLine("b / a - b = " & b / a - b)
        Console.WriteLine("b - a + b = " & b - a + b)

        Console.ReadKey()
    End Sub
End Module
