---
title: MarshalOptions, propriété – Exemple (VB)
TOCTitle: MarshalOptions property example (VB)
ms:assetid: f48ad901-7ce8-af6c-e312-51777466cd35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250241(v=office.15)
ms:contentKeyID: 48548691
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2bf801f52261d6d563f9598f6daf2257de754bdf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585605"
---
# <a name="marshaloptions-property-example-vb"></a>MarshalOptions, propriété – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [MarshalOptions](marshaloptions-property-ado.md) pour spécifier les lignes renvoyées au serveur : toutes les lignes ou uniquement les lignes modifiées.

```vb 
 
'BeginMarshalOptionsVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 
 Dim strOldFirst As String 
 Dim strOldLast As String 
 Dim strMessage As String 
 Dim strMarshalAll As String 
 Dim strMarshalModified As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' open recordset with names from Employees table 
 ' and set some properties through object refs 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.CursorType = adOpenKeyset 
 rstEmployees.LockType = adLockOptimistic 
 rstEmployees.CursorLocation = adUseClient 
 
 strSQLEmployees = "SELECT fname, lname FROM Employee ORDER BY lname" 
 
 rstEmployees.Open strSQLEmployees, Cnxn, , , adCmdText 
 ' empty properties have been set above 
 
 ' Store original data 
 strOldFirst = rstEmployees!fname 
 strOldLast = rstEmployees!lname 
 
 ' Change data in edit buffer 
 rstEmployees!fname = "Linda" 
 rstEmployees!lname = "Kobara" 
 
 ' Show contents of buffer and get user input 
 strMessage = "Edit in progress:" & vbCr & _ 
 " Original data = " & strOldFirst & " " & _ 
 strOldLast & vbCr & " Data in buffer = " & _ 
 rstEmployees!fname & " " & rstEmployees!lname & vbCr & vbCr & _ 
 "Use Update to replace the original data with " & _ 
 "the buffered data in the Recordset?" 
 strMarshalAll = "Would you like to send all the rows " & _ 
 "in the recordset back to the server?" 
 strMarshalModified = "Would you like to send only " & _ 
 "modified rows back to the server?" 
 
 If MsgBox(strMessage, vbYesNo) = vbYes Then 
 If MsgBox(strMarshalAll, vbYesNo) = vbYes Then 
 rstEmployees.MarshalOptions = adMarshalAll 
 rstEmployees.Update 
 ElseIf MsgBox(strMarshalModified, vbYesNo) = vbYes Then 
 rstEmployees.MarshalOptions = adMarshalModifiedOnly 
 rstEmployees.Update 
 End If 
 End If 
 
 ' sShow the resulting data 
 MsgBox "Data in recordset = " & rstEmployees!fname & " " & _ 
 rstEmployees!lname 
 
 ' restore original data because this is a demonstration 
 If Not (strOldFirst = rstEmployees!fname And _ 
 strOldLast = rstEmployees!lname) Then 
 rstEmployees!fname = strOldFirst 
 rstEmployees!lname = strOldLast 
 rstEmployees.Update 
 End If 
 
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
'EndMarshalOptionsVB 
```

