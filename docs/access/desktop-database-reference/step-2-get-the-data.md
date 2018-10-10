---
title: 'Étape 2 : obtenir les données'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4b93eb3e3679fdbc235f4406b0480ad2597d25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469347"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="018b4-102">Étape 2 : obtenir les données</span><span class="sxs-lookup"><span data-stu-id="018b4-102">Step 2: Get the Data</span></span>


<span data-ttu-id="018b4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="018b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="018b4-104">Étape 2 : obtenir les données</span><span class="sxs-lookup"><span data-stu-id="018b4-104">Step 2: Get the Data</span></span>

<span data-ttu-id="018b4-p101">Cette étape consiste à écrire le code permettant d'ouvrir un objet **Recordset** ADO et de préparer son envoi au client. Ouvrez le fichier XMLResponse.asp dans un éditeur de texte, tel que le Bloc-notes de Windows, puis insérez-y le code suivant :</span><span class="sxs-lookup"><span data-stu-id="018b4-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="018b4-107">Veillez à modifier la valeur du paramètre Source de données dans le paramètre de ligne strCon sur le nom de votre ordinateur Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="018b4-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="018b4-108">Gardez le fichier ouvert et passez à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="018b4-108">Keep the file open and go on to the next step.</span></span>

<span data-ttu-id="018b4-109">**Suivant** [Étape 3 : envoyer les données](step-3-send-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="018b4-109">**Next** [Step 3: Send the Data](step-3-send-the-data.md)</span></span>

