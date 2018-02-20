## Exercises 
----
Let do some exercises on every we have cover so far.

1. A program that ask 5 numbers to the user and then display them one by one, then give the smallest and biggest number.
```vbnet
Module Module1
    Sub Main()
        ' where numbers from user will be store
        Dim numbers(4) As Integer
        For i As Integer = 0 To 4
            Console.Write("Enter the " & i + 1 & " number : ")
            numbers(i) = Console.ReadLine()
        Next
        ' We are here if the is already finish iterating
        ' Display all numbers
        Console.WriteLine("-------------")
        For i As Integer = 0 To numbers.Length - 1
            Console.WriteLine("the " & i + 1 & " number you gave was : " & numbers(i))
        Next
        Console.WriteLine("---------------")
        Console.WriteLine("The smallest number is : " & numbers.Min())
        Console.WriteLine("The biggest number is : " & numbers.Max())
        Console.ReadKey()
    End Sub
End Module
```
output :
```
Enter the 1 number : 74
Enter the 2 number : 100
Enter the 3 number : 5
Enter the 4 number : 21
Enter the 5 number : 24
-------------
the 1 number you gave was : 74
the 2 number you gave was : 100
the 3 number you gave was : 5
the 4 number you gave was : 21
the 5 number you gave was : 24
---------------
The smallest number is : 5
The biggest number is : 100
```
Edit the above program so that it's will also display the sum.

2. Write a program that ask for 10 score and then calculate the average and grade.

*Grade :*

0 - 49 :  F

50 - 60 : P

61 - 74 : S

75 - 80 : D 

3. What will be the output of the following program
```vbnet
Module Module1
    Sub Main()
       Dim names() As String = {"Ali", "Meda", "joseph", "Alex"}
        For i As Integer = 0 To names.Length - 2
            If i > 1 Then
                Console.WriteLine(i)
            End If
        Next
    End Sub
End Module    
```

4. The below program does not run, please fix out code's mistake.
```vbnet
Module Module1
    Sub Main()
       Dim city As String = {"paris", "marseille", "lion"}
        For cityName As Integer in city
            Console.WriteLine("City : " & cityName)
        Next
    End Sub
End Module
```

5. Students with their gender are store in a two dimensional array your job is to display female's name only.
```vbnet
Module Module1
    Sub Main()
        Dim students(,) = {{"Peter", "Male"}, {"Alex", "Male"}, {"Marie", "Female"}, {"Michael", "Male"}, {"Rose", "Female"}}
        ' Write your code to display girls only.
    End Sub
End Module
```

6. Write program that ask the user 5 names, and if the user enter more then one time, then must display error and exit the loop


7. Write a program that will ask the user enter five people names with their age and sex, and display people names with an age greater then 18


8. Display duplicated elements
```vbnet
Module Module1
    Sub Main()
        Dim test() As Integer = {41, 74, 30, 52, 41, 62, 75, 52}
        ' As you can see the above array contain duplicate element
        ' Write code that will display those duplicate element
    End Sub
End Module
```

9. Write a program that will ask the user to enter ay number, the search that element in *myDataBase* if it's found then display *Found* otherwise display *Not found*.
If the user enter the word *stop* then exit the loop
```vbnet
Module Module1
    Sub Main()
        Dim myDataBase() As String = {"alex", "alan", "conors", "iris", "peter", "helene", "rachel", "rose", "keren"}
        While True
            ' Your code goes here.
            ' Note : this is an infinite loop it will never stop unless you stop it, when the user will enter the word stop.

        End While
    End Sub
End Module 
```