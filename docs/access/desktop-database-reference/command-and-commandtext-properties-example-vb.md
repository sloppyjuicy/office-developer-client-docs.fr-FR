---
title: Command et CommandText, propriétés - Exemple (VB)
TOCTitle: Command and CommandText Properties Example (VB)
ms:assetid: 6bf35604-401b-0727-85e8-ac2ecda368df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249425(v=office.15)
ms:contentKeyID: 48545462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0614e0bdd539abf237b78cae42386a3cb070ca41
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471624"
---
# <a name="command-and-commandtext-properties-example-vb"></a><span data-ttu-id="6fbe4-102">Command et CommandText, propriétés - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="6fbe4-102">Command and CommandText Properties Example (VB)</span></span>


<span data-ttu-id="6fbe4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fbe4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6fbe4-104">Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) pour mettre à jour le texte d'une procédure.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-104">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a procedure.</span></span>

```vb 
 
' BeginProcedureTextVB 
Sub Main() 
 On Error GoTo ProcedureTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the Command 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Update the CommandText 
 cmd.CommandText = "Select CustomerId, CompanyName, ContactName " & _ 
 "From Customers " & _ 
 "Where CustomerId = [CustId]" 
 
 ' Update the Procedure 
 Set cat.Procedures("CustomerById").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureTextError: 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProcedureTextVB 
```

