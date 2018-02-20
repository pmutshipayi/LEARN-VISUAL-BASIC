## Arrays and Collections
---
### **Arrays**
An array is a container object that holds a fixed number of values of a single type. The length of an array is established when the array is created. After creation, its length is fixed. In a simple way an array is just variable that can contain multiple values unlike a simple variable.

Syntax :
```
Dim name_of_variable As DataType = {value1, value2, ...}
```
Example :
```vbnet
Dim x() As Integer = {4, 5 , 15, 95}
Dim students() As String = {"Marie", "Peter", "Helene"}
' Declare an array but initialize it later
Dim countries(2) As String
countries(0) = "Italy"
countries(1) = "Germany"
countries(2) = "France"
```
We can not print out the array in *Console.WriteLine()* or *Console.Write()* as we do for simple variable.

```vbnet
 Console.WriteLine(students)
```
output:
```
System.String[]
```
It doesn't display elements stored in array but just display the data type of the array.

So to access any element of the array we must specify the position (index) of the element. for example :
```vbnet
students(2)
```
output :
```
Helene
```
We start counting the index from 0
```vbnet
x(0)
```
output :
```
4
```
But can show all the elements in array by using a loop

__*Using For Loop :*__
```vbnet
For i As Integer = 0 To 2
    Console.WriteLine(students(i))
Next
```
output :
```
Marie 
Peter 
Helene
```
Remember that *i* will be counting from 0 to 2
```
students(0) = Marie
students(1) = Peter
students(2) = Helene
```
__*Using Do Loop :*__
```vbnet
Dim i As Integer = 0
Do While (i < 3)
   Console.WriteLine(students(i))
   i += 1
Loop
```
output :
```
Marie 
Peter 
Helene
```
__*Using For each Loop :*__
In the precious section we didn't talk about **For each loop**, because this loop is only used on arrays and collection.

Syntax :
```
For Each element [ As datatype ] In group  
    [ statements ]  
    [ Continue For ]  
    [ statements ]  
    [ Exit For ]  
    [ statements ]  
Next [ element ]  
```

```vbnet
For Each studentName As String In students
    Console.WriteLine(studentName)
Next
```
output :
```
Marie 
Peter 
Helene
```

**Properties of The Array**
Name | Description
-----|------------
IsFixedSize |Gets a value indicating whether the Array has a fixed size.
IsReadOnly |Gets a value indicating whether the Array is read-only
Length | Gets the total number of elements in all the dimensions of the Array.
Long Length | Gets a 64-bit integer that represents the total number of elements in all the dimensions of the Array.
Rank | Gets the rank (number of dimensions) of the Array. For example, a one-dimensional array returns 1, a two-dimensional array returns 2, and so on.
SyncRoot|Gets an object that can be used to synchronize access to the Array.
IsSynchronized|Gets a value indicating whether access to the Array is synchronized (thread safe).
Go [here](https://msdn.microsoft.com/en-us/library/system.array(v=vs.110).aspx) for more details.

Let try some properties 
```vbnet
Console.WriteLine("IsFixedSize : " & students.IsFixedSize)
Console.WriteLine("IsReadOnly : " & students.IsReadOnly)
Console.WriteLine("Length : " & students.Length)
Console.WriteLine("IsSynchronized : " & students.IsSynchronized)
```
output :
```
IsFixedSize : True
IsReadOnly : False
Length : 3
IsSynchronized : False
```

**Methods :**
Name | Description
----- | ---------
BinarySearch(Array, Object) | Searches an entire one-dimensional sorted array for a specific element, using the IComparable interface implemented by each element of the array and by the specified object.
Clear(Array, Int32, Int32) | Sets a range of elements in an array to the default value of each element type.
ConstrainedCopy(Array, Int32, Array, Int32, Int32) |Copies a range of elements from an Array starting at the specified source index and pastes them to another Array starting at the specified destination index. Guarantees that all changes are undone if the copy does not succeed completely.
ConvertAll<TInput, TOutput>(TInput[], Converter<TInput, TOutput>) | Converts an array of one type to an array of another type.
Copy(Array, Array, Int32)|Copies a range of elements from an Array starting at the first element and pastes them into another Array starting at the first element. The length is specified as a 32-bit integer.
IndexOf(Array, Object) |Searches for the specified object and returns the index of its first occurrence in a one-dimensional array.
SetValue(Object, Int32)|Sets a value to the element at the specified position in the one-dimensional Array. The index is specified as a 32-bit integer.
Sort(Array) | Sorts the elements in an entire one-dimensional Array using the IComparable implementation of each element of the Array.
Go [here](https://msdn.microsoft.com/en-us/library/system.array(v=vs.110).aspx) for more details.

example :

Sorting an array
```vbnet
Dim x() As Integer = {8, 41, 0, 74, -1, 4, 25, 452}
Array.Sort(x)
For Each y As Integer In x
    Console.WriteLine(y)
Next
```
output :
```
-1
0
4
8
25
41
74
452
```
Get the sum of elements in an array
```vbnet
Dim x() As Integer = {8, 40}
Console.WriteLine(x.Sum())
```
output :
```
48
```
Get the smallest and biggest elements in an array
```vbnet
Dim x() As Integer = {8, 41, 0, 74, -1, 4, 452, 12}
Console.WriteLine("Smallest : " & x.Min())
Console.WriteLine("Biggest : " & x.Max())
```
output :
```
Smallest : -1
Biggest : 452
```

__*Modify elements in an Array :*__

We gonna now try to add or modify elements in an array after it has been declare.

Has we saw previously for accessing an element in array we must specify the index of the element, it's also the case here
```vbnet
Dim x() As Integer = {8, 41, 0, 74, -1, 4, 25, 452}
' Modify the element at index 2 of x
x(2) = 10
Console.WriteLine(x(2))
```
output :
```
10
```
In the above example we modified the element at index 2 that was *0* we changed it to *10*

__*Searching in an array :*__

Other things we can do is searching an element in array.

*Using Contains method*
```vbnet
Dim x() As Integer = {8, 41, 0, 74, -1, 4, 25, 452}
' Searching for 410
Console.WriteLine(x.Contains(410))
' Searching for -1
Console.WriteLine(x.Contains(-1))
```
output :
```
False
True
```
The above method only search one elements in an array, let try to create something to will search for more then 1 element.
```vbnet
' This code, will search for element containing in both x and y
Dim x() As Integer = {20, 85, 62, 41}
Dim y() As Integer = {93, -5, 20, 85}

For Each elementX As Integer In x
    ' Search elementX in y
    For Each elementY As Integer In y
        If elementX = elementY Then
            Console.WriteLine(elementX & " is found in x and y")
         End If
    Next
Next
```
output :
```
20 is found in x and y
85 is found in x and y
```

__*Multi dimensional Array*__:

A multi dimensional array is a array that contain other array in it.
```vbnet
' This is a two dimensional array, all elements in the students are arrays. 
Dim students(,) = {{"Robert", 17}, {"Alan", 28}, {"Milan", 10}}
```
Accessing element in multi dimensional array
```vbnet
Console.WriteLine(students(0, 0))
Console.WriteLine(students(0, 1))
```
output :
```
Robert
17
```
Or can also declare a multidimensional array as follow :
```vbnet
' this array is populated by 3 arrays
Dim students()() = {New String() {"Robert", 17}, New String() {"Alan", 28}, New String() {"Milan", 10}}
```
```vbnet
'This select the first array in students
Console.WriteLine(students(0))
```
output :
```
System.String[]
```
```vbnet
'This select the second element in the first array of students
Console.WriteLine(students(0)(1))
```
output :
```
17
```
Iterating over the a multi dimensional array
```vbnet
Dim students()() = {New String() {"Robert", 17}, New String() {"Alan", 28}, New String() {"Milan", 10}}
For Each student() As String In students
    'student will be an array
    Console.WriteLine(student(0))
    Console.WriteLine(student(1))
    Console.WriteLine("----------")
Next
```
output :
```
Robert
17
----------
Alan
28
----------
Milan
10
----------
```
A simple example
```vbnet
Module Module1
    Sub Main()
       Dim students()() = {New String() {"Robert", 17}, New String() {"Alan", 28}, New String() {"Milan", 10}}
        Console.Write("Enter name of a student : ")
        Dim studentName As String = Console.ReadLine()
        For Each student() As String In students
            If student(0) = studentName Then
                Console.WriteLine(student(0) & " is " & student(1) & " Year old")
            End If
        Next
        Console.ReadKey()
    End Sub
End Module
```
output :
```
Enter name of a student : Alan
Alan is 28 Year old
```
### **Collections**
In computer science, a collection or container is a grouping of some variable number of data items (possibly zero) that have some shared significance to the problem being solved and need to be operated upon together in some controlled fashion.

There are various collections classes and usage in vbnet
1. ArrayList
2. SortedList
3. HashTable
4. Stack
5. Queu
6. BitArray

**ArrayList :**
```vbnet
Dim fruits As New List(Of String)
fruits.Add("Bananas")
fruits.Add("Appels")
fruits.Add("Avocado")
fruits.Add("Pineapple")

'Display element at index 2
Console.WriteLine(fruits.Item(2))
```
output :
```
Avocado
```
Iterating our list
```vbnet
For Each fruit As String In fruits
    Console.WriteLine(fruit)
Next
```
output :
```
Bananas
Appels
Avocado
Pineapple
```
Removing everything in the list
```vbnet
fruits.Clear() ' this clear the list
```
Remove an element at a specific index
```vbnet
fruits.removeAt(1) 'Remove Appels from the list
```

