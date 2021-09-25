---
title: Value, propriété – Exemple (VB)
TOCTitle: Value property example (VB)
ms:assetid: c2319a14-e86f-6dc1-b203-fd5f35ffa04f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249947(v=office.15)
ms:contentKeyID: 48547547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d325c4b986fab7fb8424ef2683f2ea971fa360fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593312"
---
# <a name="value-property-example-vb"></a>Value, propriété – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété [Value](value-property-ado.md) avec les objets [Field](field-object-ado.md) et [Property](property-object-ado.md) en affichant les valeurs de champ et de propriété de la table ***Employees***.

```vb 
 
'BeginValueVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' connection and recordset variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 ' field property variables 
 Dim fld As ADODB.Field 
 Dim prp As ADODB.Property 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "employee" 
 rstEmployees.Open strSQLEmployees, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployees, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Field values in rstEmployees" 
 
 ' Enumerate the Fields collection of the Employees table 
 For Each fld In rstEmployees.Fields 
 ' Because Value is the default property of a 
 ' Field object, the use of the actual keyword 
 ' here is optional. 
 Debug.Print " " & fld.Name & " = " & fld.Value 
 Next fld 
 
 Debug.Print "Property values in rstEmployees" 
 
 ' Enumerate the Properties collection of the Recordset object 
 For Each prp In rstEmployees.Properties 
 Debug.Print " " & prp.Name & " = " & prp.Value 
 ' because Value is the default property of a Property object 
 ' use of the actual Value keyword is optional 
 Next prp 
 
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
'EndValueVB 
```

