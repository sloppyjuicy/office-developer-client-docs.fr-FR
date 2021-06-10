---
title: Gestion des erreurs dans JScript
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f06584ef752e0be7f68b3f661fbdba50b52cd20e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292040"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="b96f8-102">Gestion des erreurs dans JScript</span><span class="sxs-lookup"><span data-stu-id="b96f8-102">Handling errors in JScript</span></span>


<span data-ttu-id="b96f8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b96f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b96f8-p101">Votre code Microsoft JScript doit vérifier la propriété **Count** de la collection **Errors** de l'objet **Connection**. Si la valeur est supérieure à 0, effectuez une itération de la collection et imprimez les valeurs tel que vous le feriez dans tout autre langage.</span><span class="sxs-lookup"><span data-stu-id="b96f8-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

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

