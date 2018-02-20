## Operator
***
In this part we are going to talk about operators.

**Arithmetic Operators :**

NO | Operator | Description | example
-- | ---------| -------     | -------
1  | + | Adds the two given operands | 10 + 9 = 19
2  | - |  Sustract the two given operands | 15 - 5 = 10
3 | * | Multiplied the two given operands | 2 * 9 = 18
4 | / | Devides the two given operands | 81 / 3 = 27
5 | Mod | Finds the remain of the two given operands | 6 mod 4 = 2

Example :
```vbnet
Dim a As integer = 20
Dim b As Integer = 10
Dim c As Integer = a + b
```

**Relational Operators:**

NO | Operator | Description | example
-- | ---------| ------------| -------
1  | > | Compared if the first operands is grater than the other operands | a > b
2 | < |  Compared if the first operands is small than the second operands | a < b
3 | >= | Compared if the first operand is greater or equal to the second operand | a >= b
4 | <= | Compared if the first operand is smaller or equal to the second operand | a <= b
5 | = | Compared if the first operand is equal to the second operand | a = b
6 | <> | Compared if the first operand and the second are different | a <> b

Example:

```vbnet
Dim d As Integer = 100
Dim e As Integer = 20
Dim f As Boolean = a < b
```
f will be equal to False because d isn't lesser than e

let now write a final program for this part

```vbnet
Module Module1
    Sub Main()
        Dim a As Integer = 20
        Dim b As Integer = 10
        Dim c As Integer = a + b

        Console.WriteLine(c)

        Dim e As Integer = 100
        Dim f As Integer = 20
        Dim g As Boolean = a < b

        Console.WriteLine(g)

        Console.ReadKey()
    End Sub
End Module
```

output :

![output](../../img/3.png)
