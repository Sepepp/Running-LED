$regfile = "m32def.dat"
$crystal = 12000000

Config Porta = Output
Led Alias Porta

Dim A As Byte
Dim B As Byte
Dim I As Byte

A = &B00000001
B = &B10000000

Do

   For I = 0 To 7 Step 1
      Gosub Abc
      If I > 7 Then I = 0
      Waitms 500
      Decr I
   Next
Loop

Abc:
Led = A Or B
Rotate A , Left , 1

If A = &B00001000 Then
   A = &B00010000
End If

Rotate B , Right , 1

If B = &B00010000 Then
   B = &B00001000
End If
Return

Dta:
Data &B00000001 , &B00000010 , &B00000100 , &B00001000 , &B00010000 , &B00100000 , &B01000000 , &B10000000
