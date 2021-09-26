---
title: Cancel, méthode – Exemple (VB)
TOCTitle: Cancel method example (VB)
ms:assetid: 80851036-3627-87c2-60ca-65629136bf28
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249547(v=office.15)
ms:contentKeyID: 48545926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 433e4cb55b0cc82dc760165fbfde8a3bc67e3673
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607002"
---
# <a name="cancel-method-example-vb"></a>Cancel, méthode – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple fait appel à la méthode [Cancel](cancel-method-ado.md) pour annuler une commande exécutée sur un objet [Connection](connection-object-ado.md) lorsque la connexion est occupée.

```vb 
 
'BeginCancelVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strCmdChange As String 
 Dim strCmdRestore As String 
 'record variables 
 Dim blnChanged As Boolean 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Define command strings 
 strCmdChange = "UPDATE titles SET type = 'self_help' WHERE type = 'psychology'" 
 strCmdRestore = "UPDATE titles SET type = 'psychology' " & _ 
 "WHERE type = 'self_help'" 
 
 ' Begin a transaction, then execute a command asynchronously 
 Cnxn.BeginTrans 
 Cnxn.Execute strCmdChange, , adAsyncExecute 
 ' do something else for a little while – 
 ' use i = 1 to 32000 to allow completion 
 Dim i As Integer 
 For i = 1 To 1000 
 i = i + i 
 Debug.Print i 
 Next i 
 
 ' If the command has NOT completed, cancel the execute and 
 ' roll back the transaction; otherwise, commit the transaction 
 If CBool(Cnxn.State And adStateExecuting) Then 
 Cnxn.Cancel 
 Cnxn.RollbackTrans 
 blnChanged = False 
 MsgBox "Update canceled." 
 Else 
 Cnxn.CommitTrans 
 blnChanged = True 
 MsgBox "Update complete." 
 End If 
 
 ' If the change was made, restore the data 
 ' because this is only a demo 
 If blnChanged Then 
 Cnxn.Execute strCmdRestore 
 MsgBox "Data restored." 
 End If 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndCancelVB 
```

