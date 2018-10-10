---
title: Inscription côté client des objets métier à utiliser avec DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f3d29d20200b6e435ffafaaa35c7f507b88b939
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470711"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="cfc9e-102">Inscription côté client des objets métier à utiliser avec DCOM</span><span class="sxs-lookup"><span data-stu-id="cfc9e-102">Registering Business Objects on the Client for Use with DCOM</span></span>


<span data-ttu-id="cfc9e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfc9e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cfc9e-p101">Les objets métier personnalisés doivent faire en sorte que le côté client puisse mapper leur nom de programme (ProgId) à un identificateur (CLSID) pouvant être utilisé avec DCOM. C'est la raison pour laquelle le ProgID de l'objet DCOM doit être inscrit dans le Registre côté client et être mappé à l'ID de classe de l'objet métier côté serveur. Ceci reste facultatif pour les autres protocoles pris en charge (HTTP, HTTPS et in-process).</span><span class="sxs-lookup"><span data-stu-id="cfc9e-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="cfc9e-107">Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe donné (« {00112233-4455-6677-8899-00AABBCCDDEE} »), assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :</span><span class="sxs-lookup"><span data-stu-id="cfc9e-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

