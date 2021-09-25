---
title: Refresh, méthode – Exemple (VB)
TOCTitle: Refresh method example (VB)
ms:assetid: d5094e57-e85e-7c65-cd28-ac04692608d0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250071(v=office.15)
ms:contentKeyID: 48547958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2a05144d3cc718f00eebe41fc2a2d539faab3770
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557910"
---
# <a name="refresh-method-example-vb"></a>Refresh, méthode – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple montre comment utiliser la méthode [Refresh](refresh-method-ado.md) pour actualiser la collection [Parameters](parameters-collection-ado.md) d'un objet [Command](command-object-ado.md) de procédure stockée.

```vb 
 
Option Explicit 
 
'BeginRefreshVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection strings 
 
 ' connection and recordset variables 
 Dim Cnxn As ADODB.Connection 
 Dim cmdByRoyalty As ADODB.Command 
 Dim rstByRoyalty As ADODB.Recordset 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 ' record variables 
 Dim intRoyalty As Integer 
 Dim strAuthorID As String 
 Dim strRoyalty As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open a command object for a stored procedure 
 ' with one parameter 
 Set cmdByRoyalty = New ADODB.Command 
 Set cmdByRoyalty.ActiveConnection = Cnxn 
 cmdByRoyalty.CommandText = "byroyalty" 
 cmdByRoyalty.CommandType = adCmdStoredProc 
 cmdByRoyalty.Parameters.Refresh 
 
 ' Get parameter value, execute the command 
 ' and store the results in a recordset 
 strRoyalty = InputBox("Enter royalty:") 
 If strRoyalty = "" Then 
 Err.Raise 1, , "You either didn't enter royalty or canceled the input box. Exit the application" 
 End If 
 
 intRoyalty = Trim(strRoyalty) 
 cmdByRoyalty.Parameters(1) = intRoyalty 
 Set rstByRoyalty = cmdByRoyalty.Execute() 
 
 ' Open the Authors table to get author names for display 
 Set rstAuthors = New ADODB.Recordset 
 strSQLAuthors = "Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenForwardOnly, adLockPessimistic, adCmdTable 
 
 ' Print current data in the recordset 
 ' and add author names 
 Debug.Print "Authors with " & intRoyalty & " percent royalty" 
 
 Do Until rstByRoyalty.EOF 
 strAuthorID = rstByRoyalty!au_id 
 Debug.Print " " & rstByRoyalty!au_id & ", "; 
 rstAuthors.Filter = "au_id = '" & strAuthorID & "'" 
 Debug.Print rstAuthors!au_fname & " "; rstAuthors!au_lname 
 rstByRoyalty.MoveNext 
 Loop 
 
 ' clean up 
 rstByRoyalty.Close 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstByRoyalty = Nothing 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstByRoyalty Is Nothing Then 
 If rstByRoyalty.State = adStateOpen Then rstByRoyalty.Close 
 End If 
 Set rstByRoyalty = Nothing 
 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRefreshVB 
```

