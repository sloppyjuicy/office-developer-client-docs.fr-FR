---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357434"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="1fadc-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="1fadc-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="1fadc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fadc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fadc-105">Compare deux valeurs de propriété pour déterminer si elles sont égales.</span><span class="sxs-lookup"><span data-stu-id="1fadc-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fadc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1fadc-106">Header file:</span></span>  <br/> |<span data-ttu-id="1fadc-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="1fadc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1fadc-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1fadc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1fadc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1fadc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1fadc-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1fadc-110">Called by:</span></span>  <br/> |<span data-ttu-id="1fadc-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1fadc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="1fadc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fadc-112">Parameters</span></span>

 <span data-ttu-id="1fadc-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="1fadc-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="1fadc-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de la première propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="1fadc-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="1fadc-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="1fadc-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="1fadc-116">dans Pointeur vers une structure **SPropValue** définissant la deuxième valeur de propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="1fadc-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1fadc-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1fadc-117">Return value</span></span>

 <span data-ttu-id="1fadc-118">**LPropCompareProp** renvoie l'une des valeurs suivantes pour la plupart des types de propriétés:</span><span class="sxs-lookup"><span data-stu-id="1fadc-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="1fadc-119">Inférieur à zéro si la valeur indiquée par le paramètre _lpSPropValueA_ est inférieure à celle indiquée par le paramètre _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="1fadc-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="1fadc-120">Supérieur à zéro si la valeur indiquée par _lpSPropValueA_ est supérieure à celle indiquée par _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="1fadc-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="1fadc-121">Zéro si la valeur indiquée par _lpSPropValueA_ est égale à la valeur indiquée par _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="1fadc-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="1fadc-122">Pour les types de propriétés qui n'ont pas d'ordre intrinsèque, tels que les types Boolean ou Error, la fonction **LPropCompareProp** renvoie une valeur non définie si les deux valeurs de propriété ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="1fadc-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="1fadc-123">Cette valeur non définie est différente de zéro et est cohérente entre les appels.</span><span class="sxs-lookup"><span data-stu-id="1fadc-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1fadc-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1fadc-124">Remarks</span></span>

<span data-ttu-id="1fadc-125">Utilisez la fonction **LPropCompareProp** uniquement si les types des deux propriétés à comparer sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="1fadc-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="1fadc-126">Avant d'appeler **LPropCompareProp**, une application cliente ou un fournisseur de services doit d'abord récupérer les propriétés pour les comparer à l'aide d'un appel à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="1fadc-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="1fadc-127">Lorsqu'un client ou un fournisseur appelle **LPropCompareProp**, la fonction examine d'abord les balises de propriété pour s'assurer que la comparaison des valeurs de propriété est valide.</span><span class="sxs-lookup"><span data-stu-id="1fadc-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="1fadc-128">La fonction compare ensuite les valeurs de propriété, en renvoyant une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="1fadc-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="1fadc-129">Si les valeurs de propriété ne sont pas égales, **LPropCompareProp** détermine la valeur la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="1fadc-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="1fadc-130">Les propriétés qu' **LPropCompareProp** compare n'ont pas besoin d'appartenir au même objet.</span><span class="sxs-lookup"><span data-stu-id="1fadc-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

