---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783300"
---
# <a name="feid"></a><span data-ttu-id="fa298-103">FEID</span><span class="sxs-lookup"><span data-stu-id="fa298-103">FEID</span></span>

 
  
<span data-ttu-id="fa298-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa298-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa298-105">Identificateur d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="fa298-105">Identifier for a folder.</span></span> <span data-ttu-id="fa298-106">Il contient un identificateur d’entrée et d’autres informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="fa298-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fa298-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fa298-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="fa298-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fa298-108">Members</span></span>

 <span data-ttu-id="fa298-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="fa298-109">_abFlags_</span></span>
  
> <span data-ttu-id="fa298-110">identificateur d’entrée de 4 octets pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="fa298-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="fa298-111">Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="fa298-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="fa298-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="fa298-112">_muid_</span></span>
  
> <span data-ttu-id="fa298-113">GUID qui identifie le fournisseur de banque.</span><span class="sxs-lookup"><span data-stu-id="fa298-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="fa298-114">Voir mapidefs.h pour la définition du type de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="fa298-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="fa298-115">_espace réservé_</span><span class="sxs-lookup"><span data-stu-id="fa298-115">_placeholder_</span></span>
  
> <span data-ttu-id="fa298-116">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa298-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="fa298-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="fa298-117">_ltid_</span></span>
  
> <span data-ttu-id="fa298-118">ID à long terme du dossier.</span><span class="sxs-lookup"><span data-stu-id="fa298-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa298-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa298-119">See also</span></span>



[<span data-ttu-id="fa298-120">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="fa298-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="fa298-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fa298-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fa298-122">LTID</span><span class="sxs-lookup"><span data-stu-id="fa298-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="fa298-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="fa298-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="fa298-124">SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="fa298-124">SYNC</span></span>](sync.md)

