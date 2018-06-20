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
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783369"
---
# <a name="fpropexists"></a><span data-ttu-id="df5e1-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="df5e1-103">FPropExists</span></span>

  
  
<span data-ttu-id="df5e1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df5e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df5e1-105">Recherche une balise de propriété donnée d’une interface ou d’une interface [IMAPIProp](imapipropiunknown.md) dérivé **IMAPIProp**, tels que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="df5e1-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df5e1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="df5e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="df5e1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="df5e1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="df5e1-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="df5e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="df5e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="df5e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="df5e1-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="df5e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="df5e1-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="df5e1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="df5e1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df5e1-112">Parameters</span></span>

 <span data-ttu-id="df5e1-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="df5e1-113">_pobj_</span></span>
  
> <span data-ttu-id="df5e1-114">[in] Pointeur vers l’interface **IMAPIProp** ou une interface dérivée **IMAPIProp** dans laquelle rechercher la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="df5e1-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="df5e1-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="df5e1-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="df5e1-116">[in] Balise de propriété à rechercher.</span><span class="sxs-lookup"><span data-stu-id="df5e1-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df5e1-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="df5e1-117">Return value</span></span>

<span data-ttu-id="df5e1-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="df5e1-118">TRUE</span></span> 
  
> <span data-ttu-id="df5e1-119">Une correspondance de la balise de propriété donné a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="df5e1-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="df5e1-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="df5e1-120">FALSE</span></span> 
  
> <span data-ttu-id="df5e1-121">Une correspondance de la balise de propriété donnée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="df5e1-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df5e1-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="df5e1-122">Remarks</span></span>

<span data-ttu-id="df5e1-123">Si la balise de propriété dans le paramètre _ulPropTag_ a type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="df5e1-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="df5e1-124">Dans le cas contraire, la correspondance est pour la balise de propriété entière, y compris le type.</span><span class="sxs-lookup"><span data-stu-id="df5e1-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

