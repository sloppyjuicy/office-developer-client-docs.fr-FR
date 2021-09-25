---
title: Gestion des erreurs dans JScript
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 705faa28d86838509fe020cba11cf8de637d1473
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581139"
---
# <a name="handling-errors-in-jscript"></a>Gestion des erreurs dans JScript


**S’applique à** : Access 2013, Office 2013

Votre code Microsoft JScript doit vérifier la propriété **Count** de la collection **Errors** de l'objet **Connection**. Si la valeur est supérieure à 0, effectuez une itération de la collection et imprimez les valeurs tel que vous le feriez dans tout autre langage.

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling example (JScript)</h1> 
<% 
 var cnn1 = Server.CreateObject("ADODB.Connection"); 
 var errLoop = Server.CreateObject("ADODB.Error"); 
 var strError = new String; 
 
 try 
 { 
 // Intentionally trigger an error. 
 cnn1.Open("nothing"); 
 } 
 catch(e) 
 { 
 Response.Write(e.message); 
 } 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleJS --> 
```

