---
title: MaxRecords, propriété – Exemple (VB)
TOCTitle: MaxRecords property example (VB)
ms:assetid: e0b21025-3494-81a7-d656-03b85b0102d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250142(v=office.15)
ms:contentKeyID: 48548241
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f0cdacebe9ac576d69fa07de764d6285bc2e4905
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617964"
---
# <a name="maxrecords-property-example-vb"></a>MaxRecords, propriété – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [MaxRecords](maxrecords-property-ado.md) pour ouvrir un [Recordset](recordset-object-ado.md) contenant les 10 titres les plus coûteux de la table ***Titles***.

```vb 
 
'BeginMaxRecordsVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstTitles As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset containing the 10 most expensive 
 ' titles in the Titles table 
 Set rstTitles = New ADODB.Recordset 
 rstTitles.MaxRecords = 10 
 
 strSQLTitles = "SELECT Title, Price FROM Titles ORDER BY Price DESC" 
 rstTitles.Open strSQLTitles, strCnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' Display the contents of the recordset 
 Debug.Print "Top Ten Titles by Price:" 
 
 Do Until rstTitles.EOF 
 Debug.Print " " & rstTitles!Title & " - " & rstTitles!Price 
 rstTitles.MoveNext 
 Loop 
 
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
'EndMaxRecordsVB 
```

