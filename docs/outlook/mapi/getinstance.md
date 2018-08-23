---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579262"
---
# <a name="getinstance"></a><span data-ttu-id="fc559-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="fc559-103">GetInstance</span></span>

  
  
<span data-ttu-id="fc559-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc559-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc559-105">Copie une valeur dans une propriété à valeurs multiples sur une propriété à valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="fc559-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc559-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fc559-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc559-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="fc559-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="fc559-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fc559-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc559-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc559-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc559-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fc559-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc559-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fc559-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="fc559-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc559-112">Parameters</span></span>

 <span data-ttu-id="fc559-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="fc559-113">_pvalMv_</span></span>
  
> <span data-ttu-id="fc559-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définition d’une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="fc559-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="fc559-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="fc559-115">_pvalSv_</span></span>
  
> <span data-ttu-id="fc559-116">[in] Pointeur vers une propriété à valeur unique de recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="fc559-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="fc559-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="fc559-117">_uliInst_</span></span>
  
> <span data-ttu-id="fc559-118">[in] Le numéro d’instance, c'est-à-dire, l’élément de tableau, de la valeur en cours de copie de la structure indiquée par le paramètre _pvalMv_ .</span><span class="sxs-lookup"><span data-stu-id="fc559-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc559-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc559-119">Return value</span></span>

<span data-ttu-id="fc559-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fc559-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc559-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc559-121">Remarks</span></span>

<span data-ttu-id="fc559-122">Si la valeur copiée est trop volumineux pour la mémoire allouée, la fonction **GetInstance** copie uniquement des pointeurs au lieu d’allouer davantage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fc559-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

