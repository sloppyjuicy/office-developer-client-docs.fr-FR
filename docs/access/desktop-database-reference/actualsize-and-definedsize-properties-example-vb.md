---
title: ActualSize et DefinedSize, propriétés – Exemple (VB)
TOCTitle: ActualSize and DefinedSize properties example (VB)
ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15)
ms:contentKeyID: 48548884
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 719c9cb4361d8c43211697a8723267142fb546d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586221"
---
# <a name="actualsize-and-definedsize-properties-example-vb"></a>ActualSize et DefinedSize, propriétés – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [ActualSize](actualsize-property-ado.md) et [DefinedSize](definedsize-property-ado.md) pour afficher la taille définie et la taille réelle d'un champ.

```vb 
 
'BeginActualSizeVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstStores As ADODB.Recordset 
 Dim SQLStores As String 
 Dim strCnxn As String 
 'record variables 
 Dim strMessage As String 
 
 ' Open a recordset for the Stores table 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Set rstStores = New ADODB.Recordset 
 
 SQLStores = "Suppliers" 
 rstStores.Open SQLStores, strCnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines of code are identical as the default values for 
 'CursorType and LockType arguments match those indicated 
 
 ' Loop through the recordset displaying the contents 
 ' of the store_name field, the field's defined size, 
 ' and its actual size. 
 rstStores.MoveFirst 
 
 Do Until rstStores.EOF 
 strMessage = "Company name: " & rstStores!CompanyName & _ 
 vbCrLf & "Defined size: " & _ 
 rstStores!CompanyName.DefinedSize & _ 
 vbCrLf & "Actual size: " & _ 
 rstStores!CompanyName.ActualSize & vbCrLf 
 
 MsgBox strMessage, vbOKCancel, "ADO ActualSize Property (Visual Basic)" 
 rstStores.MoveNext 
 Loop 
 
 ' clean up 
 rstStores.Close 
 Set rstStores = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstStores Is Nothing Then 
 If rstStores.State = adStateOpen Then rstStores.Close 
 End If 
 Set rstStores = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActualSizeVB 
```

