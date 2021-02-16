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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418721"
---
# <a name="getinstance"></a><span data-ttu-id="26d9b-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="26d9b-103">GetInstance</span></span>

  
  
<span data-ttu-id="26d9b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26d9b-105">Copie une valeur dans une propriété à valeurs multiples dans une propriété à valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="26d9b-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26d9b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="26d9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="26d9b-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="26d9b-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="26d9b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="26d9b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26d9b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="26d9b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="26d9b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="26d9b-110">Called by:</span></span>  <br/> |<span data-ttu-id="26d9b-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="26d9b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="26d9b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26d9b-112">Parameters</span></span>

 <span data-ttu-id="26d9b-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="26d9b-113">_pvalMv_</span></span>
  
> <span data-ttu-id="26d9b-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="26d9b-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="26d9b-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="26d9b-115">_pvalSv_</span></span>
  
> <span data-ttu-id="26d9b-116">[in] Pointeur vers une propriété à valeur unique pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="26d9b-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="26d9b-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="26d9b-117">_uliInst_</span></span>
  
> <span data-ttu-id="26d9b-118">[in] Numéro d’instance, c’est-à-dire, l’élément de tableau, de la valeur copiée à partir de la structure indiquée par le _paramètre pvalMv._</span><span class="sxs-lookup"><span data-stu-id="26d9b-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26d9b-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="26d9b-119">Return value</span></span>

<span data-ttu-id="26d9b-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="26d9b-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26d9b-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="26d9b-121">Remarks</span></span>

<span data-ttu-id="26d9b-122">Si la valeur copiée est trop importante pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d’allouer une nouvelle mémoire.</span><span class="sxs-lookup"><span data-stu-id="26d9b-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

