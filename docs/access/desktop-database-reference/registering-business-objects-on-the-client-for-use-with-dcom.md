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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307081"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="783e1-102">Inscription d’objets métiers sur le client pour une utilisation avec DCOM</span><span class="sxs-lookup"><span data-stu-id="783e1-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="783e1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="783e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="783e1-p101">Les objets métier personnalisés doivent faire en sorte que le côté client puisse mapper leur nom de programme (ProgId) à un identificateur (CLSID) pouvant être utilisé avec DCOM. C'est la raison pour laquelle le ProgID de l'objet DCOM doit être inscrit dans le Registre côté client et être mappé à l'ID de classe de l'objet métier côté serveur. Ceci reste facultatif pour les autres protocoles pris en charge (HTTP, HTTPS et in-process).</span><span class="sxs-lookup"><span data-stu-id="783e1-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="783e1-107">Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe donné (« {00112233-4455-6677-8899-00AABBCCDDEE} »), assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :</span><span class="sxs-lookup"><span data-stu-id="783e1-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

