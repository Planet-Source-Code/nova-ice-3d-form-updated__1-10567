<div align="center">

## Nova Ice 3D Form \(Updated\!\)


</div>

### Description

I made this to make a Form 3D,I've looked at others on PSC but none were reall, so i cooked one up. hope you like.Now you can choose how big the the 3d is(i worded it wrong youll see what i mean though)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Intermediate
**User Rating**    |4.4 (22 globes from 5 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Custom Controls/ Forms/  Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__1-4.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/nova-ice-3d-form-updated__1-10567/archive/master.zip)





### Source Code

```
Sub Form_3D(frmForm As Form,LineWidth as long)
Const cPi = 3.1415926 'Perfect
Dim intLineWidth As Integer
intLineWidth = linewidth
Dim intSaveScaleMode As Integer
intSaveScaleMode = frmForm.ScaleMode
frmForm.ScaleMode = 3
Dim intScaleWidth As Integer
Dim intScaleHeight As Integer
intScaleWidth = frmForm.ScaleWidth
intScaleHeight = frmForm.ScaleHeight
frmForm.Cls
frmForm.Line (0, intScaleHeight)-(intLineWidth, 0), &HFFFFFF, BF
frmForm.Line (0, intLineWidth)-(intScaleWidth, 0), &HFFFFFF, BF
frmForm.Line (intScaleWidth, 0)-(intScaleWidth - intLineWidth, intScaleHeight), &H808080, BF
frmForm.Line (intScaleWidth, intScaleHeight - intLineWidth)-(0, intScaleHeight), &H808080, BF
Dim intCircleWidth As Integer
intCircleWidth = Sqr(intLineWidth * intLineWidth + intLineWidth * intLineWidth)
frmForm.FillStyle = 0
frmForm.FillColor = QBColor(15)
frmForm.Circle (intLineWidth, intScaleHeight - intLineWidth), intCircleWidth, QBColor(15), -3.1415926, -3.90953745777778 '-180 * cPi / 180, -224 * cPi / 180
frmForm.Circle (intScaleWidth - intLineWidth, intLineWidth), intCircleWidth, QBColor(15), -0.78539815, -1.5707963 ' -45 * cPi / 180, -90 * cPi / 180
frmForm.Line (0, intScaleHeight)-(0, 0), 0
frmForm.Line (0, 0)-(intScaleWidth - 1, 0), 0
frmForm.Line (intScaleWidth - 1, 0)-(intScaleWidth - 1, intScaleHeight - 1), 0
frmForm.Line (0, intScaleHeight - 1)-(intScaleWidth - 1, intScaleHeight - 1), 0
frmForm.ScaleMode = intSaveScaleMode
End Sub
```

