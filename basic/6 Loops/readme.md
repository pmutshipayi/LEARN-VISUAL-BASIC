## Loops
---
In computer programming, a loop is a sequence of instructions that is continually repeated until a certain condition is reached. Typically, a certain process is done, such as getting an item of data and changing it, and then some condition is checked such as whether a counter has reached a prescribed number.

Loops   | Descrptions
------    |-----------
For Loop | In computer science, a for-loop (or simply for loop) is a control flow statement for specifying iteration, which allows code to be executed repeatedly. ... This allows the body of the for-loop (the code that is being repeatedly executed) to know about the sequencing of each iteration.
Do while | Required unless Until is used. Repeat the loop until condition is False.
Do until | Required unless While is used. Repeat the loop until condition is True.
For each loop | The for-each loop is used to access each successive value in a collection of values. Arrays and Collections. It's commonly used to iterate over an array or a Collections class (eg, ArrayList). Iterable<E>. It can also iterate over anything that implements the Iterable<E> interface (must define iterator() method).


**For loop** :

Syntax :
```
For counter [ As datatype ] = start To end [ Step step ]  
    [ statements ]  
    [ Continue For ]  
    [ statements ]  
    [ Exit For ]  
    [ statements ]  
Next [ counter ] 
```
Example :
```vbnet
  For i As Integer = 0 To 10
    Console.WriteLine(i)
  Next
```
Output : 
```
0
1
2
3
4
5
6
7
8
9
10
```
That mean *i* start couting from 0 and when it reach *10* the loop exited. the above code is equivent to :
```vbnet
For i As Integer = 0 To 10 Step 1
    Console.WriteLine(i)
Next
```
You will notice that when the loop is iterating it actually adding 1 to *i* because we are using *step 1*, Let change the step and see what will append
```vbnet
For i As Integer = 0 To 10 step 2
    Console.WriteLine(i)
Next
```
output :
```
0
2
4
6
8
10
```
So now now when the loop is iterating it now adding +2 to *i*
We can even reverse our loop to count from the biggest number to the smallest one.

```vbnet
For i As Integer = 10 To 0 Step -1
    Console.WriteLine(i)
Next
```
output : 
```
10
9
8
7
6
5
4
3
2
1
0
```
We put step *-1* so that when the loop will be iterating it will be remove 1 from *i* till *i* will become 0 and then exit the loop.

**Note :** If you don't specify step with a negative to be sustract in *i* that mean each till the loop will be iterating will be adding 1 to *i* and *i* will never become 0, and the loop will run to infinite and the program may crash.

**Do While / Until loop** :

Syntax :
```
Do { While | Until } condition  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop  
-or-  
Do  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop { While | Until } condition  
```
Example :
```vbnet
Dim i As Integer = 0
Do While (i < 10)
   Console.WriteLine(i)
   i += 1
Loop
```
output :
```
0
1
2
3
4
5
6
7
8
9
```
You can notice the defference in result with the *For loop*,
do not forget to add *i += 1* at the end of the loop this is an equivalent to *step* in for loop, if you do not add it the program will run to infinite and may cause your program to crash.

```vbnet
Dim i As Integer = 10
Do While (i > 0)
   Console.WriteLine(i)
   i -= 1
Loop
```
output :
```
10
9
8
7
6
5
4
3
2
1
```

```vbnet
Dim i As Integer = 10
Do
    i -= 1
    Console.WriteLine(i)
Loop Until (i < 0)
```
output :
```
9
8
7
6
5
4
3
2
1
0
-1
```
**Exiting the loop** :

Exiting the loop is the action of breaking for executing

Example :
```vbnet
For i As Integer = 0 To 100
Console.WriteLine(i)
   If i = 10 Then
        Exit For
   End If
Next
```
output : 
```
0
1
2
3
4
5
6
7
8
9
10
```
Exit the loop when *i* is equal to 10

```vbnet
Dim i As Integer = 0
Do While (i < 140)
   Console.WriteLine(i)
   If i > 3 Then
      Exit Do
   End If
Loop
```
output :
```
0
1
2
3
4
```
Exit the loop once *i* became greater than 3.

If you are using the For loop must exit by writing :
```vbnet
Exit for
```
And for Do loop you must exist as follow :
```vbnet
Exit do
```

**Examples :**

A program that ask to user to given the number where the computer should start couting and where it should stop
```vbnet
Module Module1
    Sub Main()
        Console.Write("Count from : ")
        Dim start As Integer = Console.ReadLine()
        Console.Write("Stop at : ")
        Dim stopAt As Integer = Console.ReadLine()
        For i = start To stopAt
            Console.WriteLine("Count : " & i)
        Next
        Console.ReadKey()
    End Sub
End Module
```
output :
```
Count from : 4
Stop at : 15
Count : 4
Count : 5
Count : 6
Count : 7
Count : 8
Count : 9
Count : 10
Count : 11
Count : 12
Count : 13
Count : 14
Count : 15
```
Done for this section but we din't talk about **For each loop**, don't worry it's really useless to explain this loop here, we will do it in the next section.