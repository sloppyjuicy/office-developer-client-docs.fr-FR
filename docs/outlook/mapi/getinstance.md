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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299544"
---
# <a name="getinstance"></a><span data-ttu-id="dc35d-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="dc35d-103">GetInstance</span></span>

  
  
<span data-ttu-id="dc35d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc35d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc35d-105">Copie une valeur d'une propriété à valeurs multiples dans une propriété à valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="dc35d-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc35d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dc35d-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc35d-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="dc35d-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="dc35d-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="dc35d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc35d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc35d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc35d-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="dc35d-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc35d-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="dc35d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="dc35d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc35d-112">Parameters</span></span>

 <span data-ttu-id="dc35d-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="dc35d-113">_pvalMv_</span></span>
  
> <span data-ttu-id="dc35d-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="dc35d-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="dc35d-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="dc35d-115">_pvalSv_</span></span>
  
> <span data-ttu-id="dc35d-116">dans Pointeur vers une propriété à valeur unique qui doit recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="dc35d-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="dc35d-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="dc35d-117">_uliInst_</span></span>
  
> <span data-ttu-id="dc35d-118">dans Le numéro d'instance, autrement dit, l'élément de tableau, de la valeur copiée à partir de la structure indiquée par le paramètre _pvalMv_ .</span><span class="sxs-lookup"><span data-stu-id="dc35d-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc35d-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dc35d-119">Return value</span></span>

<span data-ttu-id="dc35d-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dc35d-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc35d-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc35d-121">Remarks</span></span>

<span data-ttu-id="dc35d-122">Si la valeur copiée est trop grande pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d'allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dc35d-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

