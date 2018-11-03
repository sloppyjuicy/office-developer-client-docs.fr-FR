---
title: Inscription des objets métier du client pour utilisent avec DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2746ad6d0736f4415788cde477e1513d9b46146
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946803"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Inscription des objets métier du client pour utilisent avec DCOM

**S’applique à**: Access 2013, Office 2013

Les objets métier personnalisés doivent faire en sorte que le côté client puisse mapper leur nom de programme (ProgId) à un identificateur (CLSID) pouvant être utilisé avec DCOM. C'est la raison pour laquelle le ProgID de l'objet DCOM doit être inscrit dans le Registre côté client et être mappé à l'ID de classe de l'objet métier côté serveur. Ceci reste facultatif pour les autres protocoles pris en charge (HTTP, HTTPS et in-process).

Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe donné (« {00112233-4455-6677-8899-00AABBCCDDEE} »), assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

