---
title: Attributes et Name, propriétés – Exemple (VB)
TOCTitle: Attributes and Name properties example (VB)
ms:assetid: b049c03c-9add-48b7-6a0a-51d2507c8e33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249840(v=office.15)
ms:contentKeyID: 48547120
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f5fb76076c743efacbc5e1a4707c765ac9d1d952
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607254"
---
# <a name="attributes-and-name-properties-example-vb"></a>Attributes et Name, propriétés – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple affiche la valeur de la propriété [Attributes](attributes-property-ado.md) des objets [Connection](connection-object-ado.md), [Field](field-object-ado.md) et [Property](property-object-ado.md). Il utilise la propriété [Name](name-property-ado.md) pour afficher le nom de chaque objet **Field** et **Property**.

```vb 
 
'BeginAttributesVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim rstEmployees As ADODB.Recordset 
 Dim strSQLEmployee As String 
 'record variables 
 Dim adoField As ADODB.Field 
 Dim adoProp As ADODB.Property 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines openign the recordset are identical as 
 'the default values for CursorType and LockType arguments match those shown 
 
 ' Display the attributes of the connection 
 Debug.Print "Connection attributes = " & Cnxn.Attributes 
 
 ' Display the property attributes of the Employee Table 
 Debug.Print "Property attributes:" 
 For Each adoProp In rstEmployees.Properties 
 Debug.Print " " & adoProp.Name & " = " & adoProp.Attributes 
 Next adoProp 
 
 ' Display the field attributes of the Employee Table 
 Debug.Print "Field attributes:" 
 For Each adoField In rstEmployees.Fields 
 Debug.Print " " & adoField.Name & " = " & adoField.Attributes 
 Next adoField 
 
 ' Display fields of the Employee Table which are NULLABLE 
 Debug.Print "NULLABLE Fields:" 
 For Each adoField In rstEmployees.Fields 
 If CBool(adoField.Attributes And adFldIsNullable) Then 
 Debug.Print " " & adoField.Name 
 End If 
 Next adoField 
 
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
'EndAttributesVB 
```

