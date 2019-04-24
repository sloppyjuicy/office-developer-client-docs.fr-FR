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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341040"
---
# <a name="fbadprop"></a><span data-ttu-id="d7a3f-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="d7a3f-103">FBadProp</span></span>

  
  
<span data-ttu-id="d7a3f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7a3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7a3f-105">Valide une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7a3f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7a3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7a3f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d7a3f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d7a3f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d7a3f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7a3f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7a3f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7a3f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d7a3f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7a3f-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d7a3f-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="d7a3f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7a3f-112">Parameters</span></span>

 <span data-ttu-id="d7a3f-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="d7a3f-113">_lpprop_</span></span>
  
> <span data-ttu-id="d7a3f-114">[in] Structure [SPropValue](spropvalue.md) définissant la propriété à valider.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7a3f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7a3f-115">Return value</span></span>

<span data-ttu-id="d7a3f-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d7a3f-116">TRUE</span></span> 
  
> <span data-ttu-id="d7a3f-117">La propriété spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="d7a3f-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d7a3f-118">FALSE</span></span> 
  
> <span data-ttu-id="d7a3f-119">La propriété spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7a3f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7a3f-120">Remarks</span></span>

<span data-ttu-id="d7a3f-121">Un fournisseur de services peut appeler la fonction **FBadProp** pour plusieurs raisons. Par exemple, pour effectuer un appel vers la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) définissant une propriété.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="d7a3f-122">**FBadProp** valide la propriété spécifiée en fonction du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="d7a3f-123">Par exemple, si la propriété est une booléenne, la fonction **FBadProp** s’assure que sa valeur est TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="d7a3f-124">Si la propriété est binaire, **FBadProp** vérifie son pointeur et sa taille, et s’assure qu’elle est correctement allouée.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7a3f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7a3f-125">See also</span></span>



[<span data-ttu-id="d7a3f-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="d7a3f-126">FBadPropTag</span></span>](fbadproptag.md)

