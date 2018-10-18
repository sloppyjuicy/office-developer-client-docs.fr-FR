---
<<<<<<< Titre tête : attributs propriété-Exemple (VB) TOCTitle : attributs de propriété-Exemple (VB) === titre : attributs, propriété-Exemple (VB) TOCTitle : attributs, propriété-Exemple (VB)
>>>>>>> Master ms:assetid : bda5e445-6425-5daf-b182-b6f5ea044b04 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249918(v=office.15) ms:contentKeyID : ms.date 48547442 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="attributes-property-example-vb"></a>Attributes, propriété - Exemple (VB)
=======
# <a name="attributes-property-example-vb"></a>Attributes, propriété-Exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Cet exemple illustre la propriété [Attributes](attributes-property-adox.md) d'un objet [Column](column-object-adox.md). Si elle a la valeur **adColNullable**, l'utilisateur peut affecter la valeur d'une chaîne vide à un objet [Field](recordset-object-ado.md) d'un [Recordset](field-object-ado.md). L'utilisateur peut ainsi distinguer un enregistrement dont les données ne sont pas connues d'un autre dont les données ne sont pas applicables.

```vb 
 
' BeginAttributesVB 
Sub Main() 
 On Error GoTo AttributesXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim colTemp As New ADOX.Column 
 Dim rstEmployees As New Recordset 
 Dim strMessage As String 
 Dim strInput As String 
 Dim tblEmp As ADOX.Table 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';data source=" & _ 
 "'c:\Program Files\Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 Set tblEmp = cat.Tables("Employees") 
 
 ' Create a new Field object and append it to the Fields 
 ' collection of the Employees table. 
 colTemp.Name = "FaxPhone" 
 colTemp.Type = adVarWChar 
 colTemp.DefinedSize = 24 
 colTemp.Attributes = adColNullable 
 cat.Tables("Employees").Columns.Append colTemp.Name, adWChar, 24 
 
 ' Open the Employees table for updating as a Recordset 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, adLockOptimistic, adCmdTable 
 
 With rstEmployees 
 ' Get user input. 
 strMessage = "Enter fax number for " & _ 
 !FirstName & " " & !LastName & "." & vbCr & _ 
 "[? - unknown, X - has no fax]" 
 strInput = UCase(InputBox(strMessage)) 
 If strInput <> "" Then 
 Select Case strInput 
 Case "?" 
 !FaxPhone = Null 
 Case "X" 
 !FaxPhone = "" 
 Case Else 
 !FaxPhone = strInput 
 End Select 
 .Update 
 
 ' Print report. 
 Debug.Print "Name - Fax number" 
 Debug.Print !FirstName & " " & !LastName & " - "; 
 
 If IsNull(!FaxPhone) Then 
 Debug.Print "[Unknown]" 
 Else 
 If !FaxPhone = "" Then 
 Debug.Print "[Has no fax]" 
 Else 
 Debug.Print !FaxPhone 
 End If 
 End If 
 
 End If 
 
 .Close 
 End With 
 
 'Clean up 
 tblEmp.Columns.Delete colTemp.Name 
 cnn.Close 
 Set rstEmployees = Nothing 
 Set cat = Nothing 
 Set colTemp = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
AttributesXError: 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not tblEmp Is Nothing Then tblEmp.Columns.Delete colTemp.Name 
 
 Set cat = Nothing 
 Set colTemp = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndAttributesVB 
```

