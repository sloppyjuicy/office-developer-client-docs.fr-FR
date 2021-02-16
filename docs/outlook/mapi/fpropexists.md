---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429487"
---
# <a name="fpropexists"></a><span data-ttu-id="cbcb9-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="cbcb9-103">FPropExists</span></span>

  
  
<span data-ttu-id="cbcb9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbcb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbcb9-105">Recherche une balise de propriété donnée dans une interface [IMAPIProp](imapipropiunknown.md) ou une interface dérivée **d’IMAPIProp,** telle que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="cbcb9-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbcb9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cbcb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="cbcb9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cbcb9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cbcb9-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="cbcb9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cbcb9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cbcb9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cbcb9-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="cbcb9-110">Called by:</span></span>  <br/> |<span data-ttu-id="cbcb9-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="cbcb9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="cbcb9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbcb9-112">Parameters</span></span>

 <span data-ttu-id="cbcb9-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="cbcb9-113">_pobj_</span></span>
  
> <span data-ttu-id="cbcb9-114">[in] Pointeur vers l’interface ou l’interface **IMAPIProp** dérivée **d’IMAPIProp** dans laquelle rechercher la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="cbcb9-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="cbcb9-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="cbcb9-116">[in] Balise de propriété pour laquelle effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbcb9-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbcb9-117">Return value</span></span>

<span data-ttu-id="cbcb9-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="cbcb9-118">TRUE</span></span> 
  
> <span data-ttu-id="cbcb9-119">Une correspondance a été trouvée pour la balise de propriété donnée.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="cbcb9-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="cbcb9-120">FALSE</span></span> 
  
> <span data-ttu-id="cbcb9-121">Une correspondance pour la balise de propriété donnée n’a pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cbcb9-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbcb9-122">Remarks</span></span>

<span data-ttu-id="cbcb9-123">Si la balise de propriété dans le paramètre  _ulPropTag_ possède un type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="cbcb9-124">Sinon, la correspondance correspond à l’ensemble de la balise de propriété, y compris le type.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

