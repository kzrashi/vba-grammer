# シート＆ブック操作

## 1. 選択ボックス

## 2. シート＆ブック操作

```vb
Dim wb As Workbook
Set wb = ActiveWorkbook            '現在アクティブなファイルを設定
Set wb = Workbooks("ファイル名.xlsx")  'ファイル名を指定して設定

Dim ws As Worksheet
Set ws = ActiveSheet                 '現在アクティブなシート名を設定
Set ws = Worksheets(インデックス番号) '左からのインデックス番号(1始まり)を指定
Set ws = Worksheets("シート名")       'シート名を指定して設定

```
