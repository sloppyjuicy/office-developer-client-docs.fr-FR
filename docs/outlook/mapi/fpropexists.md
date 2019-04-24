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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327271"
---
# <a name="fpropexists"></a><span data-ttu-id="0fcbb-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="0fcbb-103">FPropExists</span></span>

  
  
<span data-ttu-id="0fcbb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fcbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fcbb-105">Recherche une balise de propriété donnée dans une interface [IMAPIProp](imapipropiunknown.md) ou une interface dérivée de **IMAPIProp**, telle que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0fcbb-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fcbb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0fcbb-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fcbb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0fcbb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0fcbb-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0fcbb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fcbb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fcbb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fcbb-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0fcbb-110">Called by:</span></span>  <br/> |<span data-ttu-id="0fcbb-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0fcbb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="0fcbb-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fcbb-112">Parameters</span></span>

 <span data-ttu-id="0fcbb-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="0fcbb-113">_pobj_</span></span>
  
> <span data-ttu-id="0fcbb-114">dans Pointeur vers l'interface ou l'interface **IMAPIProp** dérivée de **IMAPIProp** dans lequel rechercher la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="0fcbb-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0fcbb-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="0fcbb-116">dans Balise de propriété à rechercher.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0fcbb-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0fcbb-117">Return value</span></span>

<span data-ttu-id="0fcbb-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fcbb-118">TRUE</span></span> 
  
> <span data-ttu-id="0fcbb-119">Une correspondance pour la balise de propriété donnée a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="0fcbb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="0fcbb-120">FALSE</span></span> 
  
> <span data-ttu-id="0fcbb-121">Une correspondance pour la balise de propriété donnée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fcbb-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="0fcbb-122">Remarks</span></span>

<span data-ttu-id="0fcbb-123">Si la balise de propriété dans le paramètre _ulPropTag_ est de type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l'identificateur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="0fcbb-124">Dans le cas contraire, la correspondance est pour l'intégralité de la balise de propriété, y compris le type.</span><span class="sxs-lookup"><span data-stu-id="0fcbb-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

