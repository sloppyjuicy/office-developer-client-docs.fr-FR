---
<<<<<<< Titre tête : Command et CommandText propriétés-exemple (VB) TOCTitle : Command et CommandText propriétés-exemple (VB) === titre : Command et CommandText, propriétés-exemple (VB) TOCTitle : Command et CommandText propriétés-exemple (VB)
>>>>>>> Master ms:assetid : 6bf35604-401b-0727-85e8-ac2ecda368df ms:mtpsurl : https://msdn.microsoft.com/library/JJ249425(v=office.15) ms:contentKeyID : ms.date 48545462 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="command-and-commandtext-properties-example-vb"></a>Command et CommandText, propriétés - Exemple (VB)
=======
# <a name="command-and-commandtext-properties-example-vb"></a>Command et CommandText, propriétés-exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) pour mettre à jour le texte d'une procédure.

```vb 
 
' BeginProcedureTextVB 
Sub Main() 
 On Error GoTo ProcedureTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the Command 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Update the CommandText 
 cmd.CommandText = "Select CustomerId, CompanyName, ContactName " & _ 
 "From Customers " & _ 
 "Where CustomerId = [CustId]" 
 
 ' Update the Procedure 
 Set cat.Procedures("CustomerById").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureTextError: 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProcedureTextVB 
```

