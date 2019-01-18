---
title: Inscription d’objets métiers sur le client pour une utilisation avec DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7479eefcc975ca0fe7bb7fe0d51796d1b1f416b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705511"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Inscription d’objets métiers sur le client pour une utilisation avec DCOM

**S’applique à**: Access 2013, Office 2013

Les objets métier personnalisés doivent faire en sorte que le côté client puisse mapper leur nom de programme (ProgId) à un identificateur (CLSID) pouvant être utilisé avec DCOM. C'est la raison pour laquelle le ProgID de l'objet DCOM doit être inscrit dans le Registre côté client et être mappé à l'ID de classe de l'objet métier côté serveur. Ceci reste facultatif pour les autres protocoles pris en charge (HTTP, HTTPS et in-process).

Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe donné (« {00112233-4455-6677-8899-00AABBCCDDEE} »), assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

