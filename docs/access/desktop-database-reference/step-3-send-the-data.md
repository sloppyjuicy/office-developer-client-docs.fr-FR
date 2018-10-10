---
title: 'Étape 3 : envoyer les données'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469297"
---
# <a name="step-3-send-the-data"></a><span data-ttu-id="d92d3-102">Étape 3 : envoyer les données</span><span class="sxs-lookup"><span data-stu-id="d92d3-102">Step 3: Send the Data</span></span>


<span data-ttu-id="d92d3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d92d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="d92d3-104">Étape 3 : envoyer les données</span><span class="sxs-lookup"><span data-stu-id="d92d3-104">Step 3: Send the Data</span></span>

<span data-ttu-id="d92d3-p101">À présent que vous disposez d'un objet **Recordset**, vous devez l'envoyer au client en l'enregistrant en tant que fichier XML dans l'objet **Response** ASP. Ajoutez le code suivant au bas de XMLResponse.asp :</span><span class="sxs-lookup"><span data-stu-id="d92d3-p101">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. Add the following code to the bottom of XMLResponse.asp:</span></span>

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

<span data-ttu-id="d92d3-107">Notez que l’objet ASP **Response Group** est spécifié comme destination de la méthode du **jeu d’enregistrements** à [Enregistrer](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d92d3-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="d92d3-108">La destination de la méthode **Save** peut représenter n'importe quel objet prenant en charge l'interface **IStream**, par exemple, un objet [Stream](stream-object-ado.md) ADO ou un nom de fichier incluant le chemin d'accès complet à l'emplacement au niveau duquel est enregistré l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d92d3-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="d92d3-109">Enregistrez et fermez XMLResponse.asp avant de passer à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="d92d3-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="d92d3-110">Copiez également le fichier adovbs.inc c:\\Program Files\\Common Files\\système\\dossier Ado dans le même dossier où vous avez le fichier XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="d92d3-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

<span data-ttu-id="d92d3-111">**Suivant** [Étape 4 : recevoir les données](step-4-receive-and-display-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="d92d3-111">**Next** [Step 4: Receive the Data](step-4-receive-and-display-the-data.md)</span></span>

