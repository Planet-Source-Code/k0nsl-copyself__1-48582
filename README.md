<div align="center">

## CopySelf


</div>

### Description

Copy itself to a location specified.
 
### More Info
 
There's really nothing to know about this function other than that it can copy itself to a location specified...


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[k0nsl](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/k0nsl.md)
**Level**          |Intermediate
**User Rating**    |4.0 (16 globes from 4 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/k0nsl-copyself__1-48582/archive/master.zip)





### Source Code

```
'*needs to be compiled before it copies its self
Public Sub CopySelf(Path As String, NewName As String)
  MyPath = App.Path & "\" & App.EXEName & ".EXE"
  NewLocation = Path & "\" & NewName
  On Error Resume Next
  If LCase(MyPath) <> LCase(NewLocation) Then
  FileCopy MyPath, NewLocation
End If
End Sub
Private Sub Form_Load()
Call CopySelf("C:\", "bleh.sys")
End Sub
```

