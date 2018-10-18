---
<<<<<<< Titre tête : AbsolutePosition et CursorLocation propriétés-exemple (VB) TOCTitle : ms:assetid AbsolutePosition et CursorLocation propriétés-exemple (VB) : 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249293(v=office.15) ms : contentKeyID : ms.date 48544966 : 18/09/2015 mtps_version : v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a>AbsolutePosition et CursorLocation, propriétés - Exemple (VB)
=== titre : AbsolutePosition et CursorLocation, propriétés-exemple (VB) TOCTitle : ms:assetid d’exemple (VB) les propriétés AbsolutePosition et CursorLocation : 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249293(v=office.15) ms:contentKeyID : 48544966 MS.date : 17/10/2018 mtps_version : v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a>AbsolutePosition et CursorLocation, propriétés-exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Cet exemple montre comment la propriété [AbsolutePosition](absoluteposition-property-ado.md) peut effectuer un suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet [Recordset](recordset-object-ado.md). Il utilise la propriété [CursorLocation](cursorlocation-property-ado.md) pour activer la propriété **AbsolutePosition** en définissant le curseur sur un curseur client.

```vb 
 
'BeginAbsolutePositionVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQL As String 
 'record variables 
 Dim strMessage As String 
 
 'Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open Employee recordset with 
 ' Client-side cursor to enable AbsolutePosition property 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "employee" 
 rstEmployees.Open strSQL, strCnxn, adUseClient, adLockReadOnly, adCmdTable 
 
 ' Enumerate Recordset 
 Do While Not rstEmployees.EOF 
 ' Display current record information 
 strMessage = "Employee: " & rstEmployees!lname & vbCr & _ 
 "(record " & rstEmployees.AbsolutePosition & _ 
 " of " & rstEmployees.RecordCount & ")" 
 If MsgBox(strMessage, vbOKCancel) = vbCancel Then Exit Do 
 rstEmployees.MoveNext 
 Loop 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndAbsolutePositionVB 
```

