---
title: Gestion des erreurs dans JScript
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c264d4fb4eae460934fcd056e371607c5c0138e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860209"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="f8a43-102">Gestion des erreurs dans JScript</span><span class="sxs-lookup"><span data-stu-id="f8a43-102">Handling Errors in JScript</span></span>


<span data-ttu-id="f8a43-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8a43-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8a43-p101">Votre code Microsoft JScript doit vérifier la propriété **Count** de la collection **Errors** de l'objet **Connection**. Si la valeur est supérieure à 0, effectuez une itération de la collection et imprimez les valeurs tel que vous le feriez dans tout autre langage.</span><span class="sxs-lookup"><span data-stu-id="f8a43-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

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

