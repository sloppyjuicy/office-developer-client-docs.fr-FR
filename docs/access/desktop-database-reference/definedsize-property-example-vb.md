---
title: DefinedSize, propriété – Exemple (VB)
TOCTitle: DefinedSize property example (VB)
ms:assetid: 1bad5efa-dd23-b70d-c078-85a3be0729f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248957(v=office.15)
ms:contentKeyID: 48543551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7918ec53006702fb571b0d8e91c4f25e7686da07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585759"
---
# <a name="definedsize-property-example-vb"></a>DefinedSize, propriété – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété [DefinedSize](definedsize-property-adox.md) d’un objet [Column](column-object-adox.md). Le code redéfinit la taille de la colonne FirstName de la table **Employees** de la base de données *Northwind*. Les nouvelles valeurs du [champ](field-object-ado.md) FirstName d’un objet [Recordset](recordset-object-ado.md) basé sur la table **Employees** s’affichent ensuite. Notez que, par défaut, le champ FirstName se remplit d’espaces après que vous avez redéfini la propriété **DefinedSize**.

```vb 
 
' BeginDefinedSizeVB 
Public Sub Main() 
 On Error GoTo DefinedSizeXError 
 
 Dim rstEmployees As ADODB.Recordset 
 Dim catNorthwind As New ADOX.Catalog 
 Dim colFirstName As ADOX.Column 
 Dim colNewFirstName As New ADOX.Column 
 Dim aryFirstName() As String 
 Dim i As Integer 
 Dim strCnn As String 
 
 strCnn = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Open a Recordset for the Employees table. 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.Open "Employees", strCnn, adOpenKeyset, , adCmdTable 
 ReDim aryFirstName(rstEmployees.RecordCount) 
 
 ' Open a Catalog for the Northwind database, 
 ' using same connection as rstEmployees 
 Set catNorthwind.ActiveConnection = rstEmployees.ActiveConnection 
 
 ' Loop through the recordset displaying the contents 
 ' of the FirstName field, the field's defined size, 
 ' and its actual size. 
 ' Also store FirstName values in aryFirstName array. 
 rstEmployees.MoveFirst 
 Debug.Print " " 
 Debug.Print "Original Defined Size and Actual Size" 
 i = 0 
 Do Until rstEmployees.EOF 
 Debug.Print "Employee name: " & rstEmployees!FirstName & _ 
 " " & rstEmployees!LastName 
 Debug.Print " FirstName Defined size: " _ 
 & rstEmployees!FirstName.DefinedSize 
 Debug.Print " FirstName Actual size: " & _ 
 rstEmployees!FirstName.ActualSize 
 If Not rstEmployees!FirstName = Null Then 
 aryFirstName(i) = rstEmployees!FirstName 
 End If 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 ' Redefine the DefinedSize of FirstName in the catalog 
 Set colFirstName = catNorthwind.Tables("Employees").Columns("FirstName") 
 colNewFirstName.Name = colFirstName.Name 
 colNewFirstName.Type = colFirstName.Type 
 colNewFirstName.DefinedSize = colFirstName.DefinedSize + 1 
 
 ' Append new FirstName column to catalog 
 catNorthwind.Tables("Employees").Columns.Delete colFirstName.Name 
 catNorthwind.Tables("Employees").Columns.Append colNewFirstName 
 
 ' Open Employee table in Recordset for updating 
 rstEmployees.Open "Employees", catNorthwind.ActiveConnection, _ 
 adOpenKeyset, adLockOptimistic, adCmdTable 
 
 ' Loop through the recordset displaying the contents 
 ' of the FirstName field, the field's defined size, 
 ' and its actual size. 
 ' Also restore FirstName values from aryFirstName. 
 rstEmployees.MoveFirst 
 Debug.Print " " 
 Debug.Print "New Defined Size and Actual Size" 
 i = 0 
 Do Until rstEmployees.EOF 
 rstEmployees!FirstName = aryFirstName(i) 
 Debug.Print "Employee name: " & rstEmployees!FirstName & _ 
 " " & rstEmployees!LastName 
 Debug.Print " FirstName Defined size: " _ 
 & rstEmployees!FirstName.DefinedSize 
 Debug.Print " FirstName Actual size: " & _ 
 rstEmployees!FirstName.ActualSize 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 ' Restore original FirstName column to catalog 
 catNorthwind.Tables("Employees").Columns.Delete colNewFirstName.Name 
 catNorthwind.Tables("Employees").Columns.Append colFirstName 
 
 ' Restore original FirstName values to Employees table 
 rstEmployees.Open "Employees", catNorthwind.ActiveConnection, _ 
 adOpenKeyset, adLockOptimistic, adCmdTable 
 
 rstEmployees.MoveFirst 
 i = 0 
 Do Until rstEmployees.EOF 
 rstEmployees!FirstName = aryFirstName(i) 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 'Clean up 
 Set catNorthwind = Nothing 
 Set colNewFirstName = Nothing 
 Set colFirstName = Nothing 
 Set rstEmployees = Nothing 
 Exit Sub 
 
DefinedSizeXError: 
 Set catNorthwind = Nothing 
 Set colNewFirstName = Nothing 
 Set colFirstName = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDefinedSizeVB 
```

