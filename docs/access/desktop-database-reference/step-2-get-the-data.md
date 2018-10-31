---
title: 'Étape 2 : obtenir les données'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80dae05dc691343b3c89ce8fd3ccfe72b776984c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860328"
---
# <a name="step-2-get-the-data"></a>Étape 2 : obtenir les données


**S’applique à**: Access 2013 | Office 2013

## <a name="step-2-get-the-data"></a>Étape 2 : Obtenir des données

Cette étape consiste à écrire le code permettant d'ouvrir un objet **Recordset** ADO et de préparer son envoi au client. Ouvrez le fichier XMLResponse.asp dans un éditeur de texte, tel que le Bloc-notes de Windows, puis insérez-y le code suivant :

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

Veillez à modifier la valeur du paramètre Source de données dans le paramètre de ligne strCon sur le nom de votre ordinateur Microsoft SQL Server.

Gardez le fichier ouvert et passez à l'étape suivante.

### <a name="next-step"></a>Étape suivante

[Étape 3 : envoyer les données](step-3-send-the-data.md)

