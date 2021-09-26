---
title: Append et CreateParameter, méthodes – Exemple (JScript)
TOCTitle: Append and CreateParameter methods example (JScript)
ms:assetid: 77de4191-12f1-cd6b-1805-02546fe0a942
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249494(v=office.15)
ms:contentKeyID: 48545737
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0ab5b728a7e4870b04b46fc65bdcffc1d81ed06e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607394"
---
# <a name="append-and-createparameter-methods-example-jscript"></a>Append et CreateParameter, méthodes – Exemple (JScript)


**S’applique à** : Access 2013, Office 2013

Cet exemple fait appel aux méthodes [Append](append-method-ado.md) et [CreateParameter](createparameter-method-ado.md) pour exécuter une procédure stockée avec un paramètre d'entrée. Coupez le code suivant, collez-le dans le Bloc-notes ou dans un autre éditeur de texte, puis enregistrez-le sous le nom **AppendJS.asp**.

```javascript 
 
<!-- BeginAppendJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
<head> 
 <title>Append and CreateParameter methods example (JScript)</title> 
<style> 
<!-- 
body { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>Append and CreateParameter methods example (JScript)</h1> 
<% 
 // verify user-input 
 var iRoyalty = parseInt(Request.Form("RoyaltyValue")); 
 if (iRoyalty > -1) 
 { 
 
 // connection, recordset and command variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var Cnxn = Server.CreateObject("ADODB.Connection"); 
 var cmdByRoyalty = Server.CreateObject("ADODB.Command"); 
 var rsByRoyalty = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var strMessage; 
 
 try 
 { 
 // open connection and set cursor location 
 Cnxn.Open(strCnxn); 
 Cnxn.CursorLocation = adUseClient; 
 
 // command object initial parameters 
 cmdByRoyalty.CommandText = "byroyalty"; 
 cmdByRoyalty.CommandType = adCmdStoredProc; 
 
 // create the new parameter and append to 
 // the Command object's parameters collection 
 var prmByRoyalty = cmdByRoyalty.CreateParameter("percentage", adInteger, adParamInput); 
 cmdByRoyalty.Parameters.Append(prmByRoyalty); 
 prmByRoyalty.Value = iRoyalty; 
 
 cmdByRoyalty.ActiveConnection = Cnxn; 
 
 // execute command 
 rsByRoyalty = cmdByRoyalty.Execute(); 
 
 // display results 
 rsAuthor.Open("Authors", Cnxn); 
 
 
 while (!rsByRoyalty.EOF) 
 { 
 rsAuthor.Filter = "au_id='" + rsByRoyalty.Fields("au_id") + "'"; 
 
 // start new line 
 strMessage = "<P>"; 
 
 // recordset data 
 strMessage += rsAuthor.Fields("au_fname") + " "; 
 strMessage += rsAuthor.Fields("au_lname") + " "; 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show result 
 Response.Write(strMessage); 
 
 // et next record 
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
 
 
<form method="POST" action="AppendJS.asp" id=form1 name=form1> 
 <p align="left">Enter royalty percentage to find (e.g., 40): <input type="text" name="RoyaltyValue" size="5"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
&nbsp; 
 
 
</body> 
 
</html> 
<!-- EndAppendJS --> 
 
```

