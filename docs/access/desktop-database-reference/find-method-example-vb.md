---
title: Find, méthode – Exemple (VB)
TOCTitle: Find method example (VB)
ms:assetid: 93fa7cab-e66d-7d9c-22bb-d73b44982649
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249657(v=office.15)
ms:contentKeyID: 48546408
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7190aed24c9e0789d55e8dab1ee17803cf64816f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594229"
---
# <a name="find-method-example-vb"></a>Find, méthode – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la méthode [Find](find-method-ado.md) de l’objet [Recordset](recordset-object-ado.md) pour localiser et compter le nombre de titres de fonctions dans la base de données ***Pubs***. Il est supposé, dans l'exemple, que le fournisseur sous-jacent ne prend pas en charge de fonctionnalité similaire.

```vb 
 
'BeginFindVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim Cnxn As New ADODB.Connection 
 Dim rstTitles As New ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' record variables 
 Dim mark As Variant 
 Dim count As Integer 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with default parameters which are 
 ' sufficient to search forward through a Recordset 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "SELECT title_id FROM titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 count = 0 
 rstTitles.Find "title_id LIKE 'BU%'" 
 
 Do While Not rstTitles.EOF 
 'continue if last find succeeded 
 Debug.Print "Title ID: "; rstTitles!title_id 
 'count the last title found 
 count = count + 1 
 ' note current position 
 mark = rstTitles.Bookmark 
 rstTitles.Find "title_id LIKE 'BU%'", 1, adSearchForward, mark 
 ' above code skips current record to avoid finding the same row repeatedly; 
 ' last arg (bookmark) is redundant because Find searches from current position 
 Loop 
 
 Debug.Print "The number of business titles is " & count 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then rstTitles.Close 
 End If 
 Set rstTitles = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndFindVB 
```

