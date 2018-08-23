---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591939"
---
# <a name="meid"></a><span data-ttu-id="496a8-103">MEID</span><span class="sxs-lookup"><span data-stu-id="496a8-103">MEID</span></span>

 
  
<span data-ttu-id="496a8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="496a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="496a8-105">Identificateur pour un élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="496a8-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="496a8-106">Il contient un identificateur d’entrée et d’autres informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="496a8-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="496a8-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="496a8-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="496a8-108">Members</span><span class="sxs-lookup"><span data-stu-id="496a8-108">Members</span></span>

 <span data-ttu-id="496a8-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="496a8-109">_abFlags_</span></span>
  
> <span data-ttu-id="496a8-110">identificateur d’entrée de 4 octets pour l’élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="496a8-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="496a8-111">Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="496a8-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="496a8-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="496a8-112">_muid_</span></span>
  
> <span data-ttu-id="496a8-113">GUID qui identifie le fournisseur de banque.</span><span class="sxs-lookup"><span data-stu-id="496a8-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="496a8-114">Voir mapidefs.h pour la définition du type de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="496a8-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="496a8-115">_espace réservé_</span><span class="sxs-lookup"><span data-stu-id="496a8-115">_placeholder_</span></span>
  
> <span data-ttu-id="496a8-116">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="496a8-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="496a8-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="496a8-117">_ltidFld_</span></span>
  
> <span data-ttu-id="496a8-118">ID à long terme du dossier.</span><span class="sxs-lookup"><span data-stu-id="496a8-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="496a8-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="496a8-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="496a8-120">ID à long terme de l’élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="496a8-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="496a8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="496a8-121">See also</span></span>



[<span data-ttu-id="496a8-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="496a8-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="496a8-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="496a8-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="496a8-124">LTID</span><span class="sxs-lookup"><span data-stu-id="496a8-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="496a8-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="496a8-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="496a8-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="496a8-126">UPMSG</span></span>](upmsg.md)

