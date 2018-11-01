---
title: 'Étape 3 : envoyer les données'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5af9b24ac7edb77ceb6dea9ceb5ae8e628fa5e3b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889706"
---
# <a name="step-3-send-the-data"></a>Étape 3 : envoyer les données


**S’applique à**: Access 2013, Office 2013

## <a name="step-3-send-the-data"></a>Étape 3 : Envoyer des données

À présent que vous disposez d'un objet **Recordset**, vous devez l'envoyer au client en l'enregistrant en tant que fichier XML dans l'objet **Response** ASP. Ajoutez le code suivant au bas de XMLResponse.asp :

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

Notez que l’objet ASP **Response Group** est spécifié comme destination de la méthode du **jeu d’enregistrements** à [Enregistrer](save-method-ado.md) . La destination de la méthode **Save** peut représenter n'importe quel objet prenant en charge l'interface **IStream**, par exemple, un objet [Stream](stream-object-ado.md) ADO ou un nom de fichier incluant le chemin d'accès complet à l'emplacement au niveau duquel est enregistré l'objet **Recordset**.

Enregistrez et fermez XMLResponse.asp avant de passer à l'étape suivante. Copiez également le fichier adovbs.inc c:\\Program Files\\Common Files\\système\\dossier Ado dans le même dossier où vous avez le fichier XMLResponse.asp.

### <a name="next-step"></a>Étape suivante

[Étape 4 : Recevoir les données](step-4-receive-and-display-the-data.md)

