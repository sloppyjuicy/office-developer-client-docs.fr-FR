---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783273"
---
# <a name="fbadprop"></a><span data-ttu-id="f18fc-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f18fc-103">FBadProp</span></span>

  
  
<span data-ttu-id="f18fc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f18fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f18fc-105">Valide une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f18fc-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f18fc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f18fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="f18fc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f18fc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f18fc-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="f18fc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f18fc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f18fc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f18fc-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="f18fc-110">Called by:</span></span>  <br/> |<span data-ttu-id="f18fc-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f18fc-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="f18fc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f18fc-112">Parameters</span></span>

 <span data-ttu-id="f18fc-113">_lpProp_</span><span class="sxs-lookup"><span data-stu-id="f18fc-113">_lpprop_</span></span>
  
> <span data-ttu-id="f18fc-114">[in] Une structure [SPropValue](spropvalue.md) définit la propriété à valider.</span><span class="sxs-lookup"><span data-stu-id="f18fc-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f18fc-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f18fc-115">Return value</span></span>

<span data-ttu-id="f18fc-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f18fc-116">TRUE</span></span> 
  
> <span data-ttu-id="f18fc-117">La propriété spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f18fc-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="f18fc-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f18fc-118">FALSE</span></span> 
  
> <span data-ttu-id="f18fc-119">La propriété spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="f18fc-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f18fc-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f18fc-120">Remarks</span></span>

<span data-ttu-id="f18fc-121">Un fournisseur de services peut appeler la fonction **FBadProp** pour plusieurs raisons, par exemple pour préparer un appel à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) définition d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="f18fc-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="f18fc-122">**FBadProp** valide à la propriété spécifiée en fonction du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="f18fc-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="f18fc-123">Par exemple, si la propriété est Boolean, **FBadProp** mettre sures que sa valeur est TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="f18fc-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="f18fc-124">Si la propriété est binaire, **FBadProp** vérifie son pointeur et sa taille et permet de s’assurer qu’il est correctement alloué.</span><span class="sxs-lookup"><span data-stu-id="f18fc-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f18fc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f18fc-125">See also</span></span>



[<span data-ttu-id="f18fc-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="f18fc-126">FBadPropTag</span></span>](fbadproptag.md)

