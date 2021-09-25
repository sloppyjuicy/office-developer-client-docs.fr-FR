---
title: ActiveConnection, CommandText, CommandTimeout, propriétés - Exemple (JScript)
TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction properties example(JScript)
ms:assetid: 2a79222c-4dba-9c5a-fff7-c8dd2711801f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15)
ms:contentKeyID: 48543909
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: edbe5924bb38aa44f877075a39af7631fbcc9068
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569565"
---
# <a name="activeconnection-commandtext-commandtimeout-commandtype-size-and-direction-properties-example-jscript"></a>ActiveConnection, CommandText, CommandTimeout, CommandType, Size et Direction, propriétés – Exemple (JScript)

**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [ActiveConnection](activeconnection-property-ado.md), [CommandText](commandtext-property-ado.md), [CommandTimeout](commandtimeout-property-ado.md), [CommandType](commandtype-property-ado.md), [Size](size-property-ado.md) et [Direction](direction-property-ado.md) pour exécuter une procédure stockée. Coupez et collez le code ci-après dans le Bloc-notes ou dans un autre éditeur de texte, et enregistrez-le sous **ActiveConnectionJS.asp**.

```javascript
<!-- BeginActiveConnectionJS --> 
<%@LANGUAGE="JScript"%> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
<head> 
 <title>ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead { 
 background-color: #008080; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
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
 
<body bgcolor="White"> 
 
<% 
 var iRoyalty = parseInt(Request.Form("RoyaltyValue")); 
 // check user input 
 
 if (iRoyalty > -1) 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var cmdByRoyalty = Server.CreateObject("ADODB.Command"); 
 var rsByRoyalty = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var filter, strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 cmdByRoyalty.CommandText = "byroyalty"; 
 cmdByRoyalty.CommandType = adCmdStoredProc; 
 cmdByRoyalty.CommandTimeOut = 15; 
 
 // The stored procedure called above is as follows: 
 // CREATE PROCEDURE byroyalty 
 // @percentage int 
 // AS 
 // SELECT au_id from titleauthor 
 // WHERE titleauthor.royaltyper = @percentage 
 // GO 
 
 prmByRoyalty = Server.CreateObject("ADODB.Parameter"); 
 prmByRoyalty.Type = adInteger; 
 prmByRoyalty.Size = 3; 
 prmByRoyalty.Direction = adParamInput; 
 prmByRoyalty.Value = iRoyalty; 
 cmdByRoyalty.Parameters.Append(prmByRoyalty); 
 
 cmdByRoyalty.ActiveConnection = Cnxn; 
 
 // recordset by Command - Execute 
 rsByRoyalty = cmdByRoyalty.Execute(); 
 
 // recordset by Recordset - Open 
 rsAuthor.Open("Authors", Cnxn); 
 
 while (!rsByRoyalty.EOF) 
 { 
 // set filter 
 filter = "au_id='" + rsByRoyalty("au_id") 
 rsAuthor.Filter = filter + "'"; 
 
 // start new line 
 strMessage = "<P>"; 
 
 // get data 
 strMessage += rsAuthor("au_fname") + " "; 
 strMessage += rsAuthor("au_lname") + " "; 
 
 // end line 
 strMessage += "</P>"; 
 
 // show data 
 Response.Write(strMessage); 
 
 // get next record 
 rsByRoyalty.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsByRoyalty.State == adStateOpen) 
 rsByRoyalty.Close; 
 if (rsAuthor.State == adStateOpen) 
 rsAuthor.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsByRoyalty = null; 
 rsAuthor = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ActiveConnectionJS.asp"> 
 <p align="left">Enter royalty percentage to find (e.g., 40): <input type="text" name="RoyaltyValue" size="5"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
&nbsp; 
 
 
</body> 
 
</html> 
<!-- EndActiveConnectionJS --> 
 
```

