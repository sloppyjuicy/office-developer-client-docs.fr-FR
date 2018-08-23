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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565535"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="1a390-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="1a390-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="1a390-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a390-105">Compare deux valeurs de propriété pour déterminer si elles sont égales.</span><span class="sxs-lookup"><span data-stu-id="1a390-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a390-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1a390-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a390-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1a390-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1a390-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="1a390-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a390-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a390-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1a390-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="1a390-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a390-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1a390-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="1a390-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a390-112">Parameters</span></span>

 <span data-ttu-id="1a390-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="1a390-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="1a390-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définition de la première valeur de propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="1a390-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="1a390-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="1a390-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="1a390-116">[in] Pointeur vers une structure **SPropValue** définissant la valeur de la propriété deuxième à comparer.</span><span class="sxs-lookup"><span data-stu-id="1a390-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a390-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1a390-117">Return value</span></span>

 <span data-ttu-id="1a390-118">**LPropCompareProp** renvoie une des valeurs suivantes pour la plupart des types de propriété :</span><span class="sxs-lookup"><span data-stu-id="1a390-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="1a390-119">Inférieur à zéro si la valeur indiquée par le paramètre _lpSPropValueA_ est inférieur à celui indiqué par le paramètre _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="1a390-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="1a390-120">Supérieure à zéro si la valeur indiquée par _lpSPropValueA_ est supérieure à celle indiquée par _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="1a390-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="1a390-121">Zéro si la valeur indiquée par _lpSPropValueA_ est égale à la valeur indiquée par _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="1a390-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="1a390-122">Pour les types de propriété dont aucun classement intrinsèques, telles que booléen ou erreur, la fonction **LPropCompareProp** renvoie une valeur non définie si les deux valeurs de propriété ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="1a390-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="1a390-123">Cette valeur non définie est différente de zéro et cohérente entre les appels.</span><span class="sxs-lookup"><span data-stu-id="1a390-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a390-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a390-124">Remarks</span></span>

<span data-ttu-id="1a390-125">Utilisez la fonction **LPropCompareProp** uniquement si les types d’à comparer les deux propriétés sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="1a390-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="1a390-126">Avant d’appeler **LPropCompareProp**, une application cliente ou un fournisseur de services doit récupérons d’abord les propriétés pour la comparaison avec un appel à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="1a390-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="1a390-127">Lorsqu’un client ou fournisseur appels **LPropCompareProp**, la fonction examine en premier lieu les balises de propriété pour vous assurer que la comparaison de valeurs de propriété est valide.</span><span class="sxs-lookup"><span data-stu-id="1a390-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="1a390-128">La fonction compare ensuite les valeurs de propriété, renvoyer une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="1a390-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="1a390-129">Si les valeurs de propriété ne sont pas égales, **LPropCompareProp** détermine quel est le meilleur.</span><span class="sxs-lookup"><span data-stu-id="1a390-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="1a390-130">Les propriétés **LPropCompareProp** compare n’ont pas appartenir au même objet.</span><span class="sxs-lookup"><span data-stu-id="1a390-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

