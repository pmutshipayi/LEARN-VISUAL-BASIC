## Condition
***
Condition | Descriptions
--------- | -----------
If statement | Evaluating two Statement
If and Else statement | Evaluate two Statement, if the evaluation failed the execute statement in Else block
Nested If Statement | That mean you can use many IF statement inside other If statement
Select case | Test the value of a given value over a list
Nested case | You can put many Select case statement in other Select case statement

**IF statement** :

Syntax :
```
  If Condition Then
     code to execute goes there
  End If
```
Example :
```vbnet
  If (x < 40) Then
     Console.WriteLine("X is big than 40")
  End if
```

**IF and Else statement** :

Syntax :
```
   If Condition Then
      code to execute goes here
   Else
       otherwise execute me
   End if
```

Example :
```vbnet
   If (x < 40) Then
      Console.WriteLine("X is greater than 40")
   Else
      Console.WriteLine("X is smaller than 40")
   End if
```

**Nested IF and Else statement**

Syntax :
```
   If Condition Then
      If Condition Then
         execute code in here
      End
  Else
      execute me
   End If
```

Example :
```vbnet
   If (x < 40 ) Then
      Console.WriteLine("x is greater than 40")
      If (x < 50) Then
         Console.WriteLine("x is also greater than 50")
      End if
   Else
       Console.WriteLine("X is smaller than 40")
   End If
```

**Select case statement :**


Syntax :
```
Select Case value
       case v1
           code to be executed
       case 12
            code to be executed
End Select
```
Example  :
```vbnet
  Select Case x
         Case 40
             Console.WriteLine("x is 40")
         case 100
             Console.WriteLine("x is 100")
  End Select
```
