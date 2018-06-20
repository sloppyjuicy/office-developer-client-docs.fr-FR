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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784786"
---
# <a name="mapiuid"></a><span data-ttu-id="101c2-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="101c2-103">MAPIUID</span></span>

  
  
<span data-ttu-id="101c2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="101c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="101c2-105">Une version indépendante de l’ordre des octets d’une structure [GUID](guid.md) qui sert à identifier de manière unique un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="101c2-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="101c2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="101c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="101c2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="101c2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="101c2-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="101c2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="101c2-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="101c2-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="101c2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="101c2-110">Members</span></span>

 <span data-ttu-id="101c2-111">**Carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="101c2-111">**ab**</span></span>
  
> <span data-ttu-id="101c2-112">Tableau qui contient un identificateur de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="101c2-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="101c2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="101c2-113">Remarks</span></span>

<span data-ttu-id="101c2-114">Une structure **MAPIUID** est une structure **GUID** placer dans l’ordre d’octet Intel® processeur.</span><span class="sxs-lookup"><span data-stu-id="101c2-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="101c2-115">MAPI crée des structures **MAPIUID** d’une manière qui rend très rare ont le même identificateur de deux éléments différents.</span><span class="sxs-lookup"><span data-stu-id="101c2-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="101c2-116">Structures **MAPIUID** peuvent être stockées en tant que propriétés binaires ou en tant que fichiers, quel que soit l’ordre d’octets de l’ordinateur de stockage ou d’accéder aux informations.</span><span class="sxs-lookup"><span data-stu-id="101c2-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="101c2-117">Structures **MAPIUID** sont utilisés :</span><span class="sxs-lookup"><span data-stu-id="101c2-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="101c2-118">Pour identifier une section de profil.</span><span class="sxs-lookup"><span data-stu-id="101c2-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="101c2-119">Dans les identificateurs d’entrée du message stocker et résoudre les objets book pour identifier le fournisseur de services responsables.</span><span class="sxs-lookup"><span data-stu-id="101c2-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="101c2-120">Dans la propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.</span><span class="sxs-lookup"><span data-stu-id="101c2-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="101c2-121">Pour générer un identificateur **MAPIUID** une clé de recherche, les fournisseurs de services d’appel [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="101c2-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="101c2-122">Lorsqu’un client transmet un message sur un réseau, il doit utiliser un format de protocole ou de transmission qui ne modifie pas l’ordre d’octets de données **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="101c2-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="101c2-123">Pour plus d’informations sur l’utilisation des structures **MAPIUID** , consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="101c2-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="101c2-124">Inscription des identificateurs uniques de fournisseur de Service</span><span class="sxs-lookup"><span data-stu-id="101c2-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="101c2-125">Ordre de Transport de paramètre</span><span class="sxs-lookup"><span data-stu-id="101c2-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="101c2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="101c2-126">See also</span></span>



[<span data-ttu-id="101c2-127">GUID</span><span class="sxs-lookup"><span data-stu-id="101c2-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="101c2-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="101c2-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="101c2-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="101c2-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="101c2-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="101c2-130">MAPI Structures</span></span>](mapi-structures.md)

