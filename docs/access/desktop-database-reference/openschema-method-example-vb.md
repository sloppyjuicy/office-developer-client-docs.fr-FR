---
title: OpenSchema, méthode – Exemple (VB)
TOCTitle: OpenSchema method example (VB)
ms:assetid: 02fe101a-c2df-6454-2cca-f5833e60fc03
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248797(v=office.15)
ms:contentKeyID: 48542973
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fccddd2f9566e0cb864a7a1cb4ccddb340fd0c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873459"
---
# <a name="openschema-method-example-vb"></a><span data-ttu-id="a14fb-102">OpenSchema, méthode – Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="a14fb-102">OpenSchema method example (VB)</span></span>


<span data-ttu-id="a14fb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a14fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a14fb-104">Cet exemple utilise la méthode [OpenSchema](openschema-method-ado.md) pour afficher le nom et le type de chaque table de la base de données ***Pubs***.</span><span class="sxs-lookup"><span data-stu-id="a14fb-104">This example uses the [OpenSchema](openschema-method-ado.md) method to display the name and type of each table in the ***Pubs*** database.</span></span>

```vb 
 
'BeginOpenSchemaVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub OpenSchemaX() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set rstSchema = Cnxn.OpenSchema(adSchemaTables) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn.Close 
 Set rstSchema = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchemaVB 
```

<span data-ttu-id="a14fb-105">Cet exemple spécifie un tableau\_contrainte de requête de TYPE dans la méthode **OpenSchema** argument ***critère*** .</span><span class="sxs-lookup"><span data-stu-id="a14fb-105">This example specifies a TABLE\_TYPE query constraint in the **OpenSchema** method ***Criteria*** argument.</span></span> <span data-ttu-id="a14fb-106">Par conséquent, seules les informations de schéma des affichages spécifiés dans la base de données ***Pubs*** sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a14fb-106">As a result, only schema information for the Views specified in the ***Pubs*** database are returned.</span></span> <span data-ttu-id="a14fb-107">L'exemple affiche ensuite le nom et le type des différentes tables.</span><span class="sxs-lookup"><span data-stu-id="a14fb-107">The example then displays the name(s) and type(s) of each table(s).</span></span>

```vb 
 
'BeginOpenSchema2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn2 As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn2 = New ADODB.Connection 
 strCnxn = "Provider=sqloledb;" & _ 
 "Data Source=MySqlServer;Initial Catalog=Pubs;Integrated Security=SSPI; " 
 Cnxn2.Open strCnxn 
 
 Set rstSchema = Cnxn2.OpenSchema(adSchemaTables, Array(Empty, Empty, Empty, "VIEW")) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn2.Close 
 Set rstSchema = Nothing 
 Set Cnxn2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchema2VB 
```

