---
title: AbsolutePosition et CursorLocation, propriétés - Exemple (JScript)
TOCTitle: AbsolutePosition and CursorLocation Properties Example (JScript)
ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15)
ms:contentKeyID: 48548142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eb0358073aed527fdd2711645d2bbca3194d7bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469268"
---
# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a><span data-ttu-id="438f4-102">AbsolutePosition et CursorLocation, propriétés - Exemple (JScript)</span><span class="sxs-lookup"><span data-stu-id="438f4-102">AbsolutePosition and CursorLocation Properties Example (JScript)</span></span>


<span data-ttu-id="438f4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="438f4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="438f4-p101">Cet exemple montre comment la propriété [AbsolutePosition](absoluteposition-property-ado.md) peut effectuer un suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet [Recordset](recordset-object-ado.md). Il utilise la propriété [CursorLocation](cursorlocation-property-ado.md) pour activer la propriété **AbsolutePosition** en définissant le curseur sur un curseur client. Coupez et collez le code ci-après dans le Bloc-notes ou un autre éditeur de texte et enregistrez-le sous **AbsolutePositionJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="438f4-p101">This example demonstrates how the [AbsolutePosition](absoluteposition-property-ado.md) property can track the progress of a loop that enumerates all the records of a [Recordset](recordset-object-ado.md). It uses the [CursorLocation](cursorlocation-property-ado.md) property to enable the **AbsolutePosition** property by setting the cursor to a client cursor. Cut and paste the following code to Notepad or another text editor, and save it as **AbsolutePositionJS.asp**.</span></span>

```javascript
<!-- BeginAbsolutePositionJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>AbsolutePosition and CursorLocation Properties Example (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>AbsolutePosition and CursorLocation Properties Example (JScript)</h1> 
<% 
 // connection and recordset variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 // display string 
 var strMessage; 
 
 try 
 { 
 // Open a recordset on the Employee table using 
 // a client-side cursor to enable AbsolutePosition property. 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("employees", strCnxn, adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Write beginning of table to the document. 
 Response.Write('<table border="0" align="center">'); 
 Response.Write('<tr class="thead2">'); 
 Response.Write("<th>AbsolutePosition</th><th>Name</th><th>Hire Date</th></tr>"); 
 
 while (!rsEmployee.EOF) 
 { 
 strMessage = ""; 
 
 // Start a new table row. 
 strMessage = '<tr class="tbody">'; 
 
 // First column in row contains AbsolutePosition value. 
 strMessage += "<td>" + rsEmployee.AbsolutePosition + " of " + rsEmployee.RecordCount + "</td>" 
 
 // First and last name are in first column. 
 strMessage += "<td>" + rsEmployee.Fields("FirstName") + " "; 
 strMessage += rsEmployee.Fields("LastName") + " " + "</td>"; 
 
 // Hire date in second column. 
 strMessage += "<td>" + rsEmployee.Fields("HireDate") + "</td>"; 
 
 // End the row. 
 strMessage += "</tr>"; 
 
 // Write line to document. 
 Response.Write(strMessage); 
 
 // Get next record. 
 rsEmployee.MoveNext; 
 } 
 
 // Finish writing document. 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 rsEmployee = null; 
 } 
%> 
 
</html> 
<!-- EndAbsolutePositionJS --> 
```

