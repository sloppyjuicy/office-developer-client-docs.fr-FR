---
title: BeginTrans, CommitTrans, RollbackTrans, méthodes - Exemple (VB)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods example (VB)
ms:assetid: 12fce322-dba7-9159-8a09-7f6daf1a80ed
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248904(v=office.15)
ms:contentKeyID: 48543357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a904c56275a66c4ba53b1b9c21e39a0f8ea6a1e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607114"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-example-vb"></a>BeginTrans, CommitTrans et RollbackTrans, méthodes – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple modifie le type de livre de tous les livres de la table ***Titles** _ de la base de données. Une fois [que la méthode BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) démarre une transaction qui isole toutes les modifications apportées à la table _ *_Titles_** , la méthode [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) enregistre les modifications. You can use the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method to undo changes that you saved using the [Update](update-method-ado.md) method.

```vb 
 
'BeginBeginTransVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim rstTitles As ADODB.Recordset 
 Dim strSQLTitles As String 
 'record variables 
 Dim strTitle As String 
 Dim strMessage As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Open recordset dynamic to allow for changes 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "Titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenDynamic, adLockPessimistic, adCmdTable 
 
 Cnxn.BeginTrans 
 
 ' Loop through recordset and prompt user 
 ' to change the type for a specified title 
 
 rstTitles.MoveFirst 
 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then 
 strTitle = rstTitles!Title 
 strMessage = "Title: " & strTitle & vbCr & _ 
 "Change type to self help?" 
 
 ' If yes, change type for the specified title 
 If MsgBox(strMessage, vbYesNo) = vbYes Then 
 rstTitles!Type = "self_help" 
 rstTitles.Update 
 End If 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Prompt user to commit all changes made 
 If MsgBox("Save all changes?", vbYesNo) = vbYes Then 
 Cnxn.CommitTrans 
 Else 
 Cnxn.RollbackTrans 
 End If 
 
 ' Print recordset 
 rstTitles.Requery 
 rstTitles.MoveFirst 
 Do While Not rstTitles.EOF 
 Debug.Print rstTitles!Title & " - " & rstTitles!Type 
 rstTitles.MoveNext 
 Loop 
 
 ' Restore original data as this is a demo 
 rstTitles.MoveFirst 
 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "self_help" Then 
 rstTitles!Type = "psychology" 
 rstTitles.Update 
 End If 
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
 
 
'EndBeginTransVB 
```

