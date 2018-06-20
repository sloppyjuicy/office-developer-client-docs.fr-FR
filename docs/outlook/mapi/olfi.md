---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ff23472254df2bd9d2195c7cf2c4258b856ec430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784925"
---
# <a name="olfi"></a><span data-ttu-id="c2ca1-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="c2ca1-103">OLFI</span></span>

  
  
<span data-ttu-id="c2ca1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2ca1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2ca1-105">File d’attente des structures de ID à long terme utilisé par le fournisseur de banque de dossiers personnels (PST) de fichier pour attribuer un ID d’entrée pour un nouveau message ou un dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c2ca1-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c2ca1-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c2ca1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c2ca1-107">Members</span></span>

 <span data-ttu-id="c2ca1-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-108">_ulVersion_</span></span>
  
- <span data-ttu-id="c2ca1-109">Numéro de version de la structure.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="c2ca1-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-110">_muidReserved_</span></span>
  
- <span data-ttu-id="c2ca1-111">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="c2ca1-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-112">_ulReserved_</span></span>
  
- <span data-ttu-id="c2ca1-113">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="c2ca1-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="c2ca1-115">Le nombre d’entrées qui sont disponibles pour l’affectation.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="c2ca1-116">Ces entrées de partagent le même identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="c2ca1-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="c2ca1-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="c2ca1-118">Le nombre d’entrées qui sont ensuite disponibles pour l’allocation.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="c2ca1-119">Ces entrées partagent le même GUID.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="c2ca1-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="c2ca1-121">À long terme ID structure, **[LTID](ltid.md)**, qui identifie l’entrée actuellement disponible pour affectation.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="c2ca1-122">La structure de code à long terme contient un GUID et un index qui identifie un objet dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="c2ca1-123">Le GUID et l’index peuvent forment un identificateur d’entrée unique pour un objet.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="c2ca1-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="c2ca1-125">Structure d’ID à long terme qui identifie l’entrée suivante disponible.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2ca1-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2ca1-126">Remarks</span></span>

<span data-ttu-id="c2ca1-127">Un ID d’entrée est un identificateur d’entrée MAPI 4 octets pour un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="c2ca1-128">Pour plus d’informations, voir la [propriété ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="c2ca1-128">For more information, see [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span></span>
  
<span data-ttu-id="c2ca1-129">Lorsqu’un fournisseur de magasins PST affecte un ID d’entrée à un nouvel objet, il doit tout d’abord un GUID qui identifie le serveur et un index qui identifie l’objet dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="c2ca1-130">Même si le GUID n’est pas unique parmi tous les identificateurs d’entrée, le GUID et l’index combinés fournissent une entrée unique.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="c2ca1-131">Cette paire GUID et l’index est suivie par une structure d’ID à long terme, **LTID**, qui fait partie de la structure **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="c2ca1-132">Le fournisseur de banque PST ne pas physiquement conserve dans **OLFI** une structure **LTID** pour chaque paire de GUID-index.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="c2ca1-133">Il conserve une structure **LTID** , *ltidAlloc* , pour la paire GUID-index disponible en premier ; un nombre, *dwAlloc* , le nombre d’entrées disponibles qui partagent ce même GUID ; et une deuxième structure **LTID** , *ltidNextAlloc* , pour la paire GUID-index disponible suivante qui a un GUID différent.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="c2ca1-134">Le fichier PST stocker fournisseur utilise la structure **OLFI** pour suivre les GUID et les index qu’il a attribuées. Un niveau virtuel, le fournisseur maintient une réserve d’un nombre de structures **LTID** qui sont prêts à être allouée.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="c2ca1-135">*dwAlloc* conserve un décompte des structures **LTID** disponibles.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="c2ca1-136">Les demandes pour les identificateurs d’entrée sont fournis dans les blocs.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="c2ca1-137">Lorsqu’il existe une demande pour un bloc, le fournisseur de banque PST vérifie s’il existe suffisamment réserve disponible en comparant la taille demandée avec *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="c2ca1-138">S’il existe des réserves suffisantes, elle renvoie le GUID et l’index *ltidAlloc* d’attribution.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="c2ca1-139">Il diminue *dwAlloc* la taille demandée, puis incrémente la taille requise de l’index de *ltidAlloc* .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="c2ca1-140">Il prépare le fournisseur de banque PST à allouer *ltidAlloc* sur la requête suivante pour un autre bloc d’identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="c2ca1-141">Notez que le GUID reste identique pour la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="c2ca1-142">Si la taille d’une requête est supérieure à *dwAlloc* , le fournisseur de banque PST essaie d’utiliser ce que cela a ensuite en réserve, comme spécifié par *dwNextAlloc* et *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="c2ca1-143">Il copie *dwNextAlloc* et *ltidNextAlloc* *dwAlloc* et *ltidAlloc* et définit *dwNextAlloc* et *ltidNextAlloc* sur NULL.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="c2ca1-144">Un fournisseur qui encapsule le fournisseur de banque PST doit vérifier régulièrement *ltidNextAlloc* pour voir si elle est NULL.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="c2ca1-145">Si tel est le cas, le fournisseur doit remplissez-la avec un nouveau GUID et réinitialiser *dwNextAlloc* afin que les identificateurs d’entrée plus peut être alloué.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2ca1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2ca1-146">See also</span></span>



[<span data-ttu-id="c2ca1-147">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c2ca1-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c2ca1-148">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="c2ca1-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c2ca1-149">LTID</span><span class="sxs-lookup"><span data-stu-id="c2ca1-149">LTID</span></span>](ltid.md)

