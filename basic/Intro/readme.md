Let's first create our first application using visual studio
1. Click new <br><br>
   ![new project](../img/v1.png)<br><br>
2. Project<br><br>
3. from tamplate choose Visual basic<br><br>
   ![vbnet](../img/v2.png)<br><br>
4. And finally choose console application<br><br>
   ![debug](../img/v3.png)<br><br>
5. And run our application by pressing **F5** or go debug button

As you have noticed that after running your program a black window appear and then disappear.
So we gonna tell our program to do not close immediately by adding the following line
```vbnet
Console.ReadKey()
```

This line will prevent our program from closing.

The whole code will be like:
```vbnet
Module Module1

    Sub Main()
        Console.ReadLine()
    End Sub

End Module
```
Then finally debug your app. you first app will look similar to this :

![First program](../img/1.png)

Congratulation you have made you first VB.NET application
