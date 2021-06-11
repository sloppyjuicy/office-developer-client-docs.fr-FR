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
# <a name="getinstance"></a><span data-ttu-id="54aeb-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="54aeb-103">GetInstance</span></span>

  
  
<span data-ttu-id="54aeb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54aeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54aeb-105">Copie une valeur dans une propriété à valeurs multiples dans une propriété à valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="54aeb-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54aeb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="54aeb-106">Header file:</span></span>  <br/> |<span data-ttu-id="54aeb-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="54aeb-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="54aeb-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="54aeb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="54aeb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="54aeb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="54aeb-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="54aeb-110">Called by:</span></span>  <br/> |<span data-ttu-id="54aeb-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="54aeb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="54aeb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="54aeb-112">Parameters</span></span>

 <span data-ttu-id="54aeb-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="54aeb-113">_pvalMv_</span></span>
  
> <span data-ttu-id="54aeb-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="54aeb-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="54aeb-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="54aeb-115">_pvalSv_</span></span>
  
> <span data-ttu-id="54aeb-116">[in] Pointeur vers une propriété à valeur unique pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="54aeb-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="54aeb-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="54aeb-117">_uliInst_</span></span>
  
> <span data-ttu-id="54aeb-118">[in] Numéro d’instance, c’est-à-dire, l’élément de tableau, de la valeur copiée à partir de la structure indiquée par le _paramètre pvalMv._</span><span class="sxs-lookup"><span data-stu-id="54aeb-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54aeb-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54aeb-119">Return value</span></span>

<span data-ttu-id="54aeb-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54aeb-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54aeb-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="54aeb-121">Remarks</span></span>

<span data-ttu-id="54aeb-122">Si la valeur copiée est trop importante pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d’allouer une nouvelle mémoire.</span><span class="sxs-lookup"><span data-stu-id="54aeb-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

