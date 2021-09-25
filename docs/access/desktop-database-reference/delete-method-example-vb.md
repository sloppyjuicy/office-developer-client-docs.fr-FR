---
title: Delete , méthode – Exemple (VB)
TOCTitle: Delete method example (VB)
ms:assetid: cea540c1-8c42-4d50-9363-cde3329da7a5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250023(v=office.15)
ms:contentKeyID: 48547791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b96042348eca1364e60721b5a8317af9e8905476
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602800"
---
# <a name="delete-method-example-vb"></a>Delete , méthode – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la méthode [Delete](delete-method-ado-recordset.md) pour supprimer un enregistrement spécifié d'un objet [Recordset](recordset-object-ado.md).

```vb 
 
'BeginDeleteVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstRoySched As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLRoySched As String 
 
 Dim strMsg As String 
 Dim strTitleID As String 
 Dim intLoRange As Integer 
 Dim intHiRange As Integer 
 Dim intRoyalty As Integer 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open RoySched table with cursor client-side 
 Set rstRoySched = New ADODB.Recordset 
 rstRoySched.CursorLocation = adUseClient 
 rstRoySched.CursorType = adOpenStatic 
 rstRoySched.LockType = adLockBatchOptimistic 
 rstRoySched.Open "SELECT * FROM roysched WHERE royalty = 20", strCnxn, , , adCmdText 
 
 ' Prompt for a record to delete 
 strMsg = "Before delete there are " & rstRoySched.RecordCount & _ 
 " titles with 20 percent royalty:" & vbCr & vbCr 
 
 Do While Not rstRoySched.EOF 
 strMsg = strMsg & rstRoySched!title_id & vbCr 
 rstRoySched.MoveNext 
 Loop 
 
 strMsg = strMsg & vbCr & vbCr & "Enter the ID of a record to delete:" 
 strTitleID = UCase(InputBox(strMsg)) 
 
 If strTitleID = "" Then 
 Err.Raise 1, , "You didn't enter any value for the record ID." 
 End If 
 
 ' Move to the record and save data so it can be restored 
 rstRoySched.Filter = "title_id = '" & strTitleID & "'" 
 
 If rstRoySched.RecordCount < 1 Then 
 Err.Raise 1, , "There is no record for the record ID you entered." 
 End If 
 
 intLoRange = rstRoySched!lorange 
 intHiRange = rstRoySched!hirange 
 intRoyalty = rstRoySched!royalty 
 
 ' Delete the record 
 rstRoySched.Delete 
 rstRoySched.UpdateBatch 
 
 ' Show the results 
 rstRoySched.Filter = adFilterNone 
 rstRoySched.Requery 
 strMsg = "" 
 strMsg = "After delete there are " & rstRoySched.RecordCount & _ 
 " titles with 20 percent royalty:" & vbCr & vbCr 
 Do While Not rstRoySched.EOF 
 strMsg = strMsg & rstRoySched!title_id & vbCr 
 rstRoySched.MoveNext 
 Loop 
 MsgBox strMsg 
 
 ' Restore the data because this is a demonstration 
 rstRoySched.AddNew 
 rstRoySched!title_id = strTitleID 
 rstRoySched!lorange = intLoRange 
 rstRoySched!hirange = intHiRange 
 rstRoySched!royalty = intRoyalty 
 rstRoySched.UpdateBatch 
 
 ' clean up 
 rstRoySched.Close 
 Set rstRoySched = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstRoySched Is Nothing Then 
 If rstRoySched.State = adStateOpen Then rstRoySched.Close 
 End If 
 Set rstRoySched = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndDeleteVB 
```

