---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279752"
---
# <a name="olfi"></a><span data-ttu-id="9f9b2-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="9f9b2-103">OLFI</span></span>

  
  
<span data-ttu-id="9f9b2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f9b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f9b2-105">File d’attente des structures d’ID à long terme utilisées par le fournisseur de magasins de dossiers personnels (PST) pour affecter un ID d’entrée pour un nouveau message ou dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9f9b2-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9f9b2-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="9f9b2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9f9b2-107">Members</span></span>

 <span data-ttu-id="9f9b2-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-108">_ulVersion_</span></span>
  
- <span data-ttu-id="9f9b2-109">Numéro de version de la structure.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="9f9b2-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-110">_muidReserved_</span></span>
  
- <span data-ttu-id="9f9b2-111">Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9f9b2-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-112">_ulReserved_</span></span>
  
- <span data-ttu-id="9f9b2-113">Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9f9b2-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="9f9b2-115">Nombre d’entrées disponibles pour l’allocation.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="9f9b2-116">Ces entrées partagent le même identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="9f9b2-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="9f9b2-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="9f9b2-118">Nombre d’entrées disponibles en plus pour l’allocation.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="9f9b2-119">Ces entrées partagent le même GUID.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="9f9b2-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="9f9b2-121">Structure d’ID à long terme, **[LTID,](ltid.md)** identifiant l’entrée actuellement disponible pour l’allocation.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="9f9b2-122">La structure d’ID à long terme contient un GUID et un index identifiant un objet dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="9f9b2-123">Ensemble, le GUID et l’index peuvent former un ID d’entrée unique pour un objet.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="9f9b2-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="9f9b2-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="9f9b2-125">Structure d’ID à long terme identifiant la prochaine entrée disponible.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f9b2-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f9b2-126">Remarks</span></span>

<span data-ttu-id="9f9b2-127">Un ID d’entrée est un identificateur d’entrée MAPI de 4 byte pour un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="9f9b2-128">Pour plus d’informations, [voir ENTRYID](https://msdn.microsoft.com/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="9f9b2-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="9f9b2-129">Lorsqu’un fournisseur de magasin PST affecte un ID d’entrée à un nouvel objet, il a d’abord besoin d’un GUID qui identifie le serveur et d’un index qui identifie l’objet dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="9f9b2-130">Même si le GUID n’est pas unique sur tous les ID d’entrée, le GUID et l’index combinés fournissent une entrée unique.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="9f9b2-131">Cette paire GUID/index est suivi par une structure d’ID à long terme, **LTID**, qui fait partie de la structure **OLFI.**</span><span class="sxs-lookup"><span data-stu-id="9f9b2-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="9f9b2-132">Le fournisseur de magasins PST ne conserve pas physiquement dans **OLFI** une structure **LTID** pour chaque paire GUID-index.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="9f9b2-133">Il conserve une structure **LTID,**  *ltidAlloc*  , pour la première paire GUID-index actuellement disponible ; un nombre,  *dwAlloc*  , du nombre d’entrées disponibles qui partagent ce même GUID ; et une deuxième structure **LTID,**  *ltidNextAlloc*  , pour la paire GUID-index disponible suivante qui a un GUID différent.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="9f9b2-134">Le fournisseur de magasins PST utilise la structure **OLFI** pour suivre les GUID et les index qu’il a distribués. À un niveau virtuel, le fournisseur conserve une réserve d’un certain nombre de structures **LTID** prêtes à être allouées.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="9f9b2-135">*dwAlloc tient*  à jour le nombre de structures **LTID** disponibles.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="9f9b2-136">Les demandes d’ID d’entrée sont des blocs.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="9f9b2-137">Lorsqu’une demande de bloc est demandée, le fournisseur de magasins PST vérifie si la réserve est suffisante en comparant la taille demandée à  *dwAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="9f9b2-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="9f9b2-138">S’il existe une réserve suffisante, elle renvoie le GUID et l’index  *dans ltidAlloc*  pour l’allocation.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="9f9b2-139">Il diminue ensuite  *dwAlloc*  par la taille demandée et incrémente l’index en  *ltidAlloc*  par la taille demandée.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="9f9b2-140">Cela prépare le fournisseur de magasin PST à allouer  *ltidAlloc*  à la demande suivante pour un autre bloc d’ID d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="9f9b2-141">Notez que le GUID reste le même pour la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="9f9b2-142">Si la taille d’une demande est supérieure à  *dwAlloc,*  le fournisseur de magasins PST tente d’utiliser ce qu’il a en réserve, comme spécifié par  *dwNextAlloc*  et  *ltidNextAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="9f9b2-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="9f9b2-143">Il copie  *dwNextAlloc*  et  *ltidNextAlloc*  vers  *dwAlloc*  et  *ltidAlloc*  respectivement, et définit  *dwNextAlloc*  et  *ltidNextAlloc*  sur NULL.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="9f9b2-144">Un fournisseur qui encapsule le fournisseur de magasin PST doit régulièrement vérifier  *ltidNextAlloc*  pour voir s’il est NULL.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="9f9b2-145">Si c’est le cas, le fournisseur doit le remplir avec un nouveau GUID et réinitialiser  *dwNextAlloc*  afin que d’autres ID d’entrée soient alloués.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f9b2-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f9b2-146">See also</span></span>



[<span data-ttu-id="9f9b2-147">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="9f9b2-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9f9b2-148">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="9f9b2-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9f9b2-149">LTID</span><span class="sxs-lookup"><span data-stu-id="9f9b2-149">LTID</span></span>](ltid.md)

