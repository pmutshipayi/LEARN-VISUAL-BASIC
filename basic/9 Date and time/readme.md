## Date and time
---
In this section we will see how to display the date and time and our program.
```vbnet
Dim today As Date = Date.Now
Console.WriteLine(today)
```
output :
```
2/20/2018 7:17:01 PM
```
The above show the current date and time
```vbnet
Dim today As Date = Date.Today
'Display the year
Console.WriteLine(today.Year)
'Display the month
Console.WriteLine(today.Month)
'And the day
Console.WriteLine(today.Day)
```
output :
```
2018
20
2
```
__**Formating data :**__

```vbnet
Imports System.Globalization
Module Module1
    Sub Main()
        Dim today As Date = Date.Today
        ' Format the date to show as Year/month/day
 
        Console.WriteLine(today.ToString("yyyy/MM/dd", CultureInfo.InvariantCulture))
    End Sub
End Module
```
DO NOT FORGET TO WRITE THIS LINE ABOVE YOUR CODE
```vbnet
Imports System.Globalization
```
output :
```
2018/02/20
```
__**Writing our own date and time :**__
```vbnet
'the first is the year (2002)
' second : month (10)
' third : day (1)
' fourth : hour (5)
' five : min (35)
' last : sec (2)
Dim d As New Date(2002, 10, 1, 5, 35, 2)
Console.WriteLine(d)
```
output :
```
10/1/2002 5:35:02 AM
```
__**Convert string to datetime :**__

```vbnet
Dim d As String = "10/12/1945"
Dim myDate As Date = Date.ParseExact(d, "dd/MM/yyyy", System.Globalization.DateTimeFormatInfo.InvariantInfo)
Console.WriteLine(myDate)
```
output :
```
12/10/1945
```
You can change the formatter if you want.
__**Date time calculation :**__

*Calculating the difference between 2 date*:
```vbnet
Dim startTime As New Date(2018, 2, 1, 5, 35, 2)
Dim endTime As Date = Date.Today
' Interval of year
Console.WriteLine(DateDiff(DateInterval.Year, startTime, endTime))
' Interval of day
Console.WriteLine(DateDiff(DateInterval.Day, startTime, endTime))
' Interval of hours
Console.WriteLine(DateDiff(DateInterval.Hour, startTime, endTime))
```
output :
```
0
18
450
```
Example :
```vbnet
Module Module1
    Sub Main()
        Console.Write("Enter your birth day (dd/MM/yyyy) : ")
        Dim birthDay As Date = Date.ParseExact(Console.ReadLine(), "dd/MM/yyyy", System.Globalization.DateTimeFormatInfo.InvariantInfo)
        Dim today As Date = Date.Now
        ' Calculating the difference
        Console.WriteLine("You are " & DateDiff(DateInterval.Year, birthDay, today) & " year old")
        Console.WriteLine("You have " & DateDiff(DateInterval.Day, birthDay, today) & " days")
        Console.WriteLine("And " & DateDiff(DateInterval.Hour, birthDay, today) & " hours")
    End Sub
End Module
```
output :
```
Enter your birth day (dd/MM/yyyy) : 25/01/1962
You are 56 year old
You have 20480 days
And 491540 hours
```