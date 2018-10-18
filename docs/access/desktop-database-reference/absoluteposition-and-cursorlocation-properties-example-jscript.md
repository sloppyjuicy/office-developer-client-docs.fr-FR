---
<<<<<<< Titre tête : AbsolutePosition et CursorLocation, propriétés-exemple (JScript) TOCTitle : AbsolutePosition et CursorLocation, propriétés-exemple (JScript) ms:assetid : dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID : ms.date 48548142 : 18/09/2015 mtps_version : v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a>AbsolutePosition et CursorLocation, propriétés - Exemple (JScript)

=== titre : AbsolutePosition et CursorLocation, propriétés-exemple (JScript) TOCTitle : ms:assetid d’exemple (JScript) les propriétés AbsolutePosition et CursorLocation : dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID : ms.date 48548142 : 17/10/2018 mtps_version : v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a>AbsolutePosition et CursorLocation, propriétés-exemple (JScript)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Cet exemple montre comment la propriété [AbsolutePosition](absoluteposition-property-ado.md) peut effectuer un suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet [Recordset](recordset-object-ado.md). Il utilise la propriété [CursorLocation](cursorlocation-property-ado.md) pour activer la propriété **AbsolutePosition** en définissant le curseur sur un curseur client. Coupez et collez le code ci-après dans le Bloc-notes ou un autre éditeur de texte et enregistrez-le sous **AbsolutePositionJS.asp**.

```javascript
<!-- BeginAbsolutePositionJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<<<<<<< HEAD
<title>AbsolutePosition and CursorLocation Properties Example (JScript)</title> 
=======
<title>AbsolutePosition and CursorLocation properties example (JScript)</title> 
>>>>>>> master
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
<<<<<<< HEAD
<h1>AbsolutePosition and CursorLocation Properties Example (JScript)</h1> 
=======
<h1>AbsolutePosition and CursorLocation properties example (JScript)</h1> 
>>>>>>> master
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

