---
title: 'Étape 4 : recevoir et afficher les données'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471783"
---
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="8faaf-102">Étape 4 : recevoir et afficher les données</span><span class="sxs-lookup"><span data-stu-id="8faaf-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="8faaf-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8faaf-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="8faaf-104">Étape 4 : recevoir et afficher les données</span><span class="sxs-lookup"><span data-stu-id="8faaf-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="8faaf-p101">Cette étape consiste à créer un fichier HTML avec un objet [RDS.DataControl](datacontrol-object-rds.md) incorporé pointant vers le fichier XMLResponse.asp pour obtenir l'objet **Recordset**. Ouvrez le fichier default.htm avec un éditeur de texte, tel que le Bloc-notes de Windows, puis ajoutez le code ci-dessous. Remplacez « sqlserver » dans l'URL par le nom de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="8faaf-p101">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**. Open default.htm with a text editor, such as Windows Notepad, and add the code below. Replace "sqlserver" in the URL with the name of your server computer.</span></span>

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

<span data-ttu-id="8faaf-108">Fermez le fichier default.htm et enregistrez-le dans le dossier où vous avez enregistré XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="8faaf-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="8faaf-109">À l’aide d’Internet Explorer 4.0 ou version ultérieure, ouvrez l’URL https://*sqlserver*/XMLPersist/default.htm et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="8faaf-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="8faaf-110">Les données s'affichent dans un tableau DHTML lié.</span><span class="sxs-lookup"><span data-stu-id="8faaf-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="8faaf-111">Ouvrez l’URL https://*sqlserver*/XMLPersist/XMLResponse.asp et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="8faaf-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="8faaf-112">Le fichier XML s'affiche.</span><span class="sxs-lookup"><span data-stu-id="8faaf-112">The XML is displayed.</span></span>

