## Exercices
***
1.Write a program that ask the user age and then display on the screen, the output should something like : You are 13

2.Write a program that ask the user the age and then display on the screen if the user is a adult or not, according to the age provided

3.Write a program that ask the user two values an then find the sum of the two values given, then display the result on the screen

4.Write a program that ask the user 3 values of data type integer and then display on the screen the biggest number only

5.What will be the output of the below program
```vbnet
Module Module1
    Sub Main()
        Dim m As Integer = 45
        Dim c As Integer = 10
        Dim k As Boolean = m < c
        If k = True Then
            Console.WriteLine("Hello")
        Else
            Console.WriteLine("Holla holla")
        End If
        Console.ReadKey()
    End Sub
End Module
```



6.What will be the output of the below program
```vbnet
Module Module1
    Sub Main()
        Dim hour As Integer = 10
        Select Case hour
            Case 0 To 12
                Console.WriteLine("Good morning")
            Case 13 To 16
                Console.WriteLine("Good afternoon")
            Case Else
                Console.WriteLine("Good evening")
        End Select
        Console.WriteLine()
    End Sub
End Module
```



8.What will be the output of the below program
```vbnet
Module Module1
    Sub Main()
        Dim message As String
        Dim age As Integer = 17
        If age >= 18 Then
            message = "You are allow to access the website"
        Else
            message = "Not allowed"
        End If
        Console.WriteLine(message)
        Console.WriteLine()
    End Sub
End Module
```


7.Fix the below program
```vbnet
   Module Module1
    Sub Main()
        Dim x As Integer = 41
        If x =< 4 Then
            Console.WriteLine(x)
        End 
    End Sub
    Console.ReadLine()
End Module
```


8.Fix the below program
```vbnet
Module Module1
    Sub Main()
        Dim x As Integer = 41
        Dim c As String = "hello"
        Console.WriteLine(c)
    Console.ReadLine()
End Module
```

9.The modify the below code to print out the value of x on the screen
```vbnet
Module Module1
    Sub Main()
        Dim x As Integer = 41
        Dim y As Double = 415.45
        Console.WriteLine("x")
        Console.ReadKey()
    End Sub
End Module
```



10.After running this program it's automatically closed, so add the code to make it DO NOT CLOSE after running it.
```vbnet
Module Module1
    Sub Main()
        Console.WriteLine("hello, world")
    End Sub
End Module
```




11.Make the variable **age** to get the age from the user, instead of providing it in source code, and then prevent the app from closing automatically after running it.
```vbnet
Module Module1
    Sub Main()
        Dim age As Integer = 19
        Dim currentYear As Integer = 2018
        Dim yearOfBorn As Integer = currentYear - age
        Console.WriteLine("You were born in " & yearOfBorn)
    End Sub
End Module
``` 