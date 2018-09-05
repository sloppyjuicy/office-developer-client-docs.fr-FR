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
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578849"
---
# <a name="fbadprop"></a><span data-ttu-id="534e7-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="534e7-103">FBadProp</span></span>

  
  
<span data-ttu-id="534e7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="534e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="534e7-105">Valide une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="534e7-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="534e7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="534e7-106">Header File</span></span>  <br/> |<span data-ttu-id="534e7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="534e7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="534e7-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="534e7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="534e7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="534e7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="534e7-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="534e7-110">Called by:</span></span>  <br/> |<span data-ttu-id="534e7-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="534e7-111">Service Providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="534e7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="534e7-112">Parameters</span></span>

 <span data-ttu-id="534e7-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="534e7-113">_lpprop_</span></span>
  
> <span data-ttu-id="534e7-114">[in] Structure [SPropValue](spropvalue.md) définissant la propriété à valider.</span><span class="sxs-lookup"><span data-stu-id="534e7-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="534e7-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="534e7-115">Return value</span></span>

<span data-ttu-id="534e7-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="534e7-116">TRUE</span></span> 
  
> <span data-ttu-id="534e7-117">La propriété spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="534e7-117">The specified property name is invalid.</span></span> 
    
<span data-ttu-id="534e7-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="534e7-118">FALSE</span></span> 
  
> <span data-ttu-id="534e7-119">La propriété spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="534e7-119">The specified unit is not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="534e7-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="534e7-120">Remarks</span></span>

<span data-ttu-id="534e7-121">Un fournisseur de services peut appeler la fonction **FBadProp** pour plusieurs raisons. Par exemple, pour effectuer un appel vers la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) définissant une propriété.</span><span class="sxs-lookup"><span data-stu-id="534e7-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="534e7-122">**FBadProp** valide la propriété spécifiée en fonction du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="534e7-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="534e7-123">Par exemple, si la propriété est une booléenne, la fonction **FBadProp** s’assure que sa valeur est TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="534e7-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="534e7-124">Si la propriété est binaire, **FBadProp** vérifie son pointeur et sa taille, et s’assure qu’elle est correctement allouée.</span><span class="sxs-lookup"><span data-stu-id="534e7-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="534e7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="534e7-125">See also</span></span>



[<span data-ttu-id="534e7-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="534e7-126">FBadPropTag</span></span>](fbadproptag.md)

