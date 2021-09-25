---
title: ActiveConnection, CommandText, CommandTimeout, propriétés - Exemple (VB)
TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction properties example (VB)
ms:assetid: dc869f6b-3c48-9fc8-ae3a-5850ed5d3274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250116(v=office.15)
ms:contentKeyID: 48548140
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3f62709fe6593dfec01c87ad5231a079ab3a2641
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586291"
---
# <a name="activeconnection-commandtext-commandtimeout-commandtype-size-and-direction-properties-example-vb"></a>ActiveConnection, CommandText, CommandTimeout, CommandType, Size et Direction, propriétés – Exemple (VB)

**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [ActiveConnection](activeconnection-property-ado.md), [CommandText](commandtext-property-ado.md), [CommandTimeout](commandtimeout-property-ado.md), [CommandType](commandtype-property-ado.md), [Size](size-property-ado.md) et [Direction](direction-property-ado.md) pour exécuter une procédure stockée.

```vb 
 
'BeginActiveConnectionVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset, command and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim cmdByRoyalty As ADODB.Command 
 Dim prmByRoyalty As ADODB.Parameter 
 Dim rstByRoyalty As ADODB.Recordset 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 Dim strSQLByRoyalty As String 
 'record variables 
 Dim intRoyalty As Integer 
 Dim strAuthorID As String 
 
 ' Define a command object for a stored procedure 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set cmdByRoyalty = New ADODB.Command 
 Set cmdByRoyalty.ActiveConnection = Cnxn 
 ' Set the criteria 
 strSQLByRoyalty = "byroyalty" 
 cmdByRoyalty.CommandText = strSQLByRoyalty 
 cmdByRoyalty.CommandType = adCmdStoredProc 
 cmdByRoyalty.CommandTimeout = 15 
 
 ' Define the stored procedure's input parameter 
 intRoyalty = Trim(InputBox("Enter royalty:")) 
 Set prmByRoyalty = New ADODB.Parameter 
 prmByRoyalty.Type = adInteger 
 prmByRoyalty.Size = 3 
 prmByRoyalty.Direction = adParamInput 
 prmByRoyalty.Value = intRoyalty 
 
 cmdByRoyalty.Parameters.Append prmByRoyalty 
 
 ' Create a recordset by executing the command. 
 Set rstByRoyalty = cmdByRoyalty.Execute() 
 
 ' Open the Authors Table to get author names for display 
 Set rstAuthors = New ADODB.Recordset 
 strSQLAuthors = "Authors" 
 
 'rstAuthors.Open strSQLAuthors, strCnxn, , , adCmdTable 
 rstAuthors.Open strSQLAuthors, strCnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines of code are identical as the default values for 
 'CursorType and LockType arguments match those shown 
 
 ' Print the recordset and add author names from Table 
 Debug.Print "Authors with " & intRoyalty & _ 
 " percent royalty" 
 
 Do Until rstByRoyalty.EOF 
 strAuthorID = rstByRoyalty!au_id 
 Debug.Print , rstByRoyalty!au_id & ", "; 
 rstAuthors.Filter = "au_id = '" & strAuthorID & "'" 
 Debug.Print rstAuthors!au_fname & " " & _ 
 rstAuthors!au_lname 
 rstByRoyalty.MoveNext 
 Loop 
 
 ' clean up 
 rstAuthors.Close 
 rstByRoyalty.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set rstByRoyalty = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not rstByRoyalty Is Nothing Then 
 If rstByRoyalty.State = adStateOpen Then rstByRoyalty.Close 
 End If 
 Set rstByRoyalty = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActiveConnectionVB 
```

