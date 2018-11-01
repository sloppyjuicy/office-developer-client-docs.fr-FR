---
title: Inscription côté client des objets métier à utiliser avec DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b106fa88df8205595312aaebdabf82cf12d57c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887809"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Inscription côté client des objets métier à utiliser avec DCOM


**S’applique à**: Access 2013, Office 2013

Les objets métier personnalisés doivent faire en sorte que le côté client puisse mapper leur nom de programme (ProgId) à un identificateur (CLSID) pouvant être utilisé avec DCOM. C'est la raison pour laquelle le ProgID de l'objet DCOM doit être inscrit dans le Registre côté client et être mappé à l'ID de classe de l'objet métier côté serveur. Ceci reste facultatif pour les autres protocoles pris en charge (HTTP, HTTPS et in-process).

Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe donné (« {00112233-4455-6677-8899-00AABBCCDDEE} »), assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

