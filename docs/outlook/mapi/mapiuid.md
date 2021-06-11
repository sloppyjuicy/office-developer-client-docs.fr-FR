---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432204"
---
# <a name="mapiuid"></a><span data-ttu-id="e43f4-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e43f4-103">MAPIUID</span></span>

  
  
<span data-ttu-id="e43f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e43f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e43f4-105">Version indépendante d’un ordre d’byte d’une structure [GUID](guid.md) utilisée pour identifier de manière unique un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e43f4-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e43f4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e43f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="e43f4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e43f4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e43f4-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="e43f4-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e43f4-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="e43f4-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="e43f4-110">Members</span><span class="sxs-lookup"><span data-stu-id="e43f4-110">Members</span></span>

 <span data-ttu-id="e43f4-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="e43f4-111">**ab**</span></span>
  
> <span data-ttu-id="e43f4-112">Tableau qui contient un identificateur de 16 byte.</span><span class="sxs-lookup"><span data-stu-id="e43f4-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e43f4-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e43f4-113">Remarks</span></span>

<span data-ttu-id="e43f4-114">Une structure **MAPIUID** est une structure **GUID** mise dans l’ordre ® processeur Intel.</span><span class="sxs-lookup"><span data-stu-id="e43f4-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="e43f4-115">MAPI crée des structures **MAPIUID** d’une manière qui rend très rare que deux éléments différents ont le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="e43f4-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="e43f4-116">Les structures **MAPIUID** peuvent être stockées en tant que propriétés binaires ou en tant que fichiers, sans prendre en compte l’ordre des bytes de l’ordinateur stockant ou accédant aux informations.</span><span class="sxs-lookup"><span data-stu-id="e43f4-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="e43f4-117">**Les structures MAPIUID** sont utilisées :</span><span class="sxs-lookup"><span data-stu-id="e43f4-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="e43f4-118">Pour identifier une section de profil.</span><span class="sxs-lookup"><span data-stu-id="e43f4-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="e43f4-119">Dans les identificateurs d’entrée des objets de magasin de messages et de carnet d’adresses pour identifier le fournisseur de services responsable.</span><span class="sxs-lookup"><span data-stu-id="e43f4-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="e43f4-120">Dans la **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.</span><span class="sxs-lookup"><span data-stu-id="e43f4-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="e43f4-121">Pour générer un **identificateur MAPIUID** pour une clé de recherche, les fournisseurs de services appellent [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="e43f4-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="e43f4-122">Lorsqu’un client transmet un message sur un réseau, il doit utiliser un format de protocole ou de transmission qui ne modifie pas l’ordre d’byte des données **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="e43f4-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="e43f4-123">Pour plus d’informations sur l’utilisation des structures **MAPIUID,** consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e43f4-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="e43f4-124">Inscription des identificateurs uniques du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="e43f4-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="e43f4-125">Définition de l’ordre de transport</span><span class="sxs-lookup"><span data-stu-id="e43f4-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="e43f4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e43f4-126">See also</span></span>



[<span data-ttu-id="e43f4-127">GUID</span><span class="sxs-lookup"><span data-stu-id="e43f4-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="e43f4-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e43f4-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="e43f4-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="e43f4-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="e43f4-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e43f4-130">MAPI Structures</span></span>](mapi-structures.md)

