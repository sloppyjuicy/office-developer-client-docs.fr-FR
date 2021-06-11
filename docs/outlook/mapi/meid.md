---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430307"
---
# <a name="meid"></a><span data-ttu-id="3c683-103">MEID</span><span class="sxs-lookup"><span data-stu-id="3c683-103">MEID</span></span>

 
  
<span data-ttu-id="3c683-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c683-105">Identificateur d’Outlook’élément.</span><span class="sxs-lookup"><span data-stu-id="3c683-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="3c683-106">Il contient un identificateur d’entrée et d’autres informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="3c683-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c683-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3c683-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="3c683-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3c683-108">Members</span></span>

 <span data-ttu-id="3c683-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="3c683-109">_abFlags_</span></span>
  
> <span data-ttu-id="3c683-110">Identificateur d’entrée de 4 Outlook’élément.</span><span class="sxs-lookup"><span data-stu-id="3c683-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="3c683-111">Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="3c683-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="3c683-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="3c683-112">_muid_</span></span>
  
> <span data-ttu-id="3c683-113">GUID qui identifie le fournisseur du magasin.</span><span class="sxs-lookup"><span data-stu-id="3c683-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="3c683-114">Voir mapidefs.h pour la définition de type **de MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="3c683-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="3c683-115">_espace réservé_</span><span class="sxs-lookup"><span data-stu-id="3c683-115">_placeholder_</span></span>
  
> <span data-ttu-id="3c683-116">Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3c683-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3c683-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="3c683-117">_ltidFld_</span></span>
  
> <span data-ttu-id="3c683-118">ID à long terme du dossier.</span><span class="sxs-lookup"><span data-stu-id="3c683-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="3c683-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="3c683-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="3c683-120">ID à long terme de l’Outlook’élément.</span><span class="sxs-lookup"><span data-stu-id="3c683-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c683-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c683-121">See also</span></span>



[<span data-ttu-id="3c683-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="3c683-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3c683-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="3c683-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3c683-124">LTID</span><span class="sxs-lookup"><span data-stu-id="3c683-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="3c683-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="3c683-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="3c683-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="3c683-126">UPMSG</span></span>](upmsg.md)

