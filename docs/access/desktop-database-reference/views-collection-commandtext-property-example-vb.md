---
<<<<<<< Titre tête : Views, Collection, exemple de propriété CommandText (VB) TOCTitle : Views, Collection, exemple de propriété CommandText (VB) === titre : Collection Views, CommandText, propriété-Exemple (VB) TOCTitle : Views, Collection CommandText, propriété-Exemple (VB)
>>>>>>> Master ms:assetid : 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249331(v=office.15) ms:contentKeyID : ms.date 48545120 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="views-collection-commandtext-property-example-vb"></a>Views, collection - Exemple de propriété CommandText (VB)
=======
# <a name="views-collection-commandtext-property-example-vb"></a>Views, Collection CommandText, propriété-Exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) pour mettre à jour le texte d'une vue.

```vb 
 
' BeginViewsCollectionVB 
Sub Main() 
 On Error GoTo ViewTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command 
 Set cmd = cat.Views("AllCustomers").Command 
 
 ' Update the CommandText of the Command 
 cmd.CommandText = _ 
 "Select CustomerId, CompanyName, ContactName From Customers" 
 
 ' Update the View 
 Set cat.Views("AllCustomers").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewTextError: 
 
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
' EndViewsCollectionVB 
```

