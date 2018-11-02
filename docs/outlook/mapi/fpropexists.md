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
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570435"
---
# <a name="fpropexists"></a><span data-ttu-id="35c80-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="35c80-103">FPropExists</span></span>

  
  
<span data-ttu-id="35c80-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35c80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35c80-105">Recherche une balise de propriété donnée d’une interface ou d’une interface [IMAPIProp](imapipropiunknown.md) dérivé **IMAPIProp**, tels que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="35c80-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35c80-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="35c80-106">Header file:</span></span>  <br/> |<span data-ttu-id="35c80-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="35c80-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="35c80-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="35c80-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35c80-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35c80-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35c80-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="35c80-110">Called by:</span></span>  <br/> |<span data-ttu-id="35c80-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="35c80-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="35c80-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35c80-112">Parameters</span></span>

 <span data-ttu-id="35c80-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="35c80-113">_pobj_</span></span>
  
> <span data-ttu-id="35c80-114">[in] Pointeur vers l’interface **IMAPIProp** ou une interface dérivée **IMAPIProp** dans laquelle rechercher la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="35c80-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="35c80-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="35c80-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="35c80-116">[in] Balise de propriété à rechercher.</span><span class="sxs-lookup"><span data-stu-id="35c80-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35c80-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35c80-117">Return value</span></span>

<span data-ttu-id="35c80-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="35c80-118">TRUE</span></span> 
  
> <span data-ttu-id="35c80-119">Une correspondance de la balise de propriété donné a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="35c80-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="35c80-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="35c80-120">FALSE</span></span> 
  
> <span data-ttu-id="35c80-121">Une correspondance de la balise de propriété donnée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="35c80-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35c80-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="35c80-122">Remarks</span></span>

<span data-ttu-id="35c80-123">Si la balise de propriété dans le paramètre _ulPropTag_ a type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="35c80-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="35c80-124">Dans le cas contraire, la correspondance est pour la balise de propriété entière, y compris le type.</span><span class="sxs-lookup"><span data-stu-id="35c80-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

