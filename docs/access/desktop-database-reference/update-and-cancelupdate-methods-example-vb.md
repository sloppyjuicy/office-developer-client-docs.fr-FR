---
title: Update et CancelUpdate, méthodes – Exemple (VB)
TOCTitle: Update and CancelUpdate methods example (VB)
ms:assetid: 8ba504b0-d3b9-41de-f8a5-09da3456ee6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249614(v=office.15)
ms:contentKeyID: 48546223
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec1938a1f42e024612c618c62c19ca16ee5678f1
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465567"
---
# <a name="update-and-cancelupdate-methods-example-vb"></a>Update et CancelUpdate, méthodes – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la méthode [Update](update-method-ado.md) conjointement à la méthode [CancelUpdate](cancelupdate-method-ado.md).

```vb 
 
'BeginUpdateVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 ' buffer variables 
 Dim strOldFirst As String 
 Dim strOldLast As String 
 Dim strMessage As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset to enable changes 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "SELECT fname, lname FROM Employee ORDER BY lname" 
 rstEmployees.Open strSQLEmployees, Cnxn, adOpenKeyset, adLockOptimistic, adCmdText 
 
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
 
 If MsgBox(strMessage, vbYesNo) = vbYes Then 
 rstEmployees.Update 
 Else 
 rstEmployees.CancelUpdate 
 End If 
 
 ' show the resulting data 
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
' EndUpdateVB 
```


Cet exemple illustre la méthode **Update** conjointement à la méthode [AddNew](addnew-method-ado.md).

```vb 
 
' BeginUpdate2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim cnn1 As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim strEmpID As String 
 Dim strOldFirst As String 
 Dim strOldLast As String 
 Dim strMessage As String 
 Dim strCnn As String 
 
 ' Open a connection. 
 Set cnn1 = New ADODB.Connection 
 strCnn = "Provider=sqloledb;" & _ 
 "Data Source=MySqlServer;Initial Catalog=Pubs;Integrated Security=SSPI; " 
 cnn1.Open strCnn 
 
 ' Open recordset with data from Employees table. 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.CursorType = adOpenKeyset 
 rstEmployees.LockType = adLockOptimistic 
 rstEmployees.Open "employee", cnn1, , , adCmdTable 
 
 rstEmployees.AddNew 
 strEmpID = "B-S55555M" 
 rstEmployees!emp_id = strEmpID 
 rstEmployees!fname = "Bill" 
 rstEmployees!lname = "Sornsin" 
 
 ' Show contents of buffer and get user input. 
 strMessage = "AddNew in progress:" & vbCr & _ 
 "Data in buffer = " & rstEmployees!emp_id & ", " & _ 
 rstEmployees!fname & " " & rstEmployees!lname & vbCr & vbCr & _ 
 "Use Update to save buffer to recordset?" 
 
 If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
 rstEmployees.Update 
 ' Go to the new record and show the resulting data. 
 MsgBox "Data in recordset = " & rstEmployees!emp_id & ", " & _ 
 rstEmployees!fname & " " & rstEmployees!lname 
 Else 
 rstEmployees.CancelUpdate 
 MsgBox "No new record added." 
 End If 
 
 ' Delete new data because this is a demonstration. 
 cnn1.Execute "DELETE FROM employee WHERE emp_id = '" & strEmpID & "'" 
 
 ' clean up 
 rstEmployees.Close 
 cnn1.Close 
 Set rstEmployees = Nothing 
 Set cnn1 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not cnn1 Is Nothing Then 
 If cnn1.State = adStateOpen Then cnn1.Close 
 End If 
 Set cnn1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndUpdate2VB 
```

