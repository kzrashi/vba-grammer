# 基本文法

## 1. デバッグ

- print("出力したい文字列")や print(出力したい変数名)を指定出力します。

```vb
Debug.print "test"
```

## 2. if 文

- 基本

```vb
If 条件式1 Then
    処理1
ElseIf 条件式2 Then
    処理2
ElseIf a = b Or _
       c = d Then
    処理3
ElseIf a = b And _
       c = d Then
    処理4
Else
    処理2
End If
```

## 3. for 文

- for 文(途中で抜ける)

```vb
Dim i As Integer
For i = 1 To 5

    If Cells(2, 1).Value = "br" Then
        Exit For
    End If

   	MsgBox "こんにちは"

Next i
```

- for 文(continue)
  `Goto`を使う

```vb
Dim r As Long

For r = 1 To 10
    If Cells(r, 1) = "" Then
        GoTo Continue
    End If

Continue:

Next r

```

## 4. switch 文

- Select Case ～ End Select を使う
- break はいらない
- 数値だけでなく、文字も判定可能

```vb
Dim morning
morning = 1
Select Case morning
    Case 1
        処理1
    Case 2
        処理2
    Case 3
        処理3
    Case Else
        Debug.Print "Zzz..."
End Select
```

## 5. while 文

- Do While ～ Loop を使う
- 途中で抜けるときは Exit Do を使う

```vb
Dim i
i = 0

Do While i < 5

    i = i + 1

    If i = 2 Then
        Exit Do
    End If

Loop

```
