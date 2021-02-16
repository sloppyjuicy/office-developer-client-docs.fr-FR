---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409810"
---
# <a name="feid"></a><span data-ttu-id="cb45c-103">FEID</span><span class="sxs-lookup"><span data-stu-id="cb45c-103">FEID</span></span>

 
  
<span data-ttu-id="cb45c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb45c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb45c-105">Identificateur d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="cb45c-105">Identifier for a folder.</span></span> <span data-ttu-id="cb45c-106">Il contient un identificateur d’entrée et d’autres informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="cb45c-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb45c-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="cb45c-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="cb45c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cb45c-108">Members</span></span>

 <span data-ttu-id="cb45c-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="cb45c-109">_abFlags_</span></span>
  
> <span data-ttu-id="cb45c-110">Identificateur d’entrée de 4 byte pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="cb45c-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="cb45c-111">Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="cb45c-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="cb45c-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="cb45c-112">_muid_</span></span>
  
> <span data-ttu-id="cb45c-113">GUID qui identifie le fournisseur du magasin.</span><span class="sxs-lookup"><span data-stu-id="cb45c-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="cb45c-114">Voir mapidefs.h pour la définition de type **de MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="cb45c-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="cb45c-115">_espace réservé_</span><span class="sxs-lookup"><span data-stu-id="cb45c-115">_placeholder_</span></span>
  
> <span data-ttu-id="cb45c-116">Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cb45c-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="cb45c-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="cb45c-117">_ltid_</span></span>
  
> <span data-ttu-id="cb45c-118">ID à long terme du dossier.</span><span class="sxs-lookup"><span data-stu-id="cb45c-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb45c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb45c-119">See also</span></span>



[<span data-ttu-id="cb45c-120">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="cb45c-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="cb45c-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="cb45c-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cb45c-122">LTID</span><span class="sxs-lookup"><span data-stu-id="cb45c-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="cb45c-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="cb45c-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="cb45c-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="cb45c-124">SYNC</span></span>](sync.md)

