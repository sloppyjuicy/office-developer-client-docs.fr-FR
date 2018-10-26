---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585121"
---
# <a name="szfindsz"></a><span data-ttu-id="1a026-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="1a026-103">SzFindSz</span></span>

  
  
<span data-ttu-id="1a026-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a026-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a026-105">Recherche la première occurrence d’une sous-chaîne terminée dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1a026-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a026-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1a026-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a026-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1a026-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1a026-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1a026-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a026-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a026-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1a026-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1a026-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a026-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1a026-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="1a026-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a026-112">Parameters</span></span>

 <span data-ttu-id="1a026-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="1a026-113">_lpsz_</span></span>
  
> <span data-ttu-id="1a026-114">[in] Pointeur vers la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1a026-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="1a026-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="1a026-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="1a026-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="1a026-116">_lpszKey_</span></span>
  
> <span data-ttu-id="1a026-117">[in] Pointeur vers la sous-chaîne terminée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1a026-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="1a026-118">Le paramètre _lpszKey_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="1a026-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a026-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a026-119">Return value</span></span>

 <span data-ttu-id="1a026-120">**SzFindSz** retourne un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1a026-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="1a026-121">Si la sous-chaîne ne se produit pas n’importe où dans la chaîne, si _lpszKey_ est supérieure à _lpsz_, ou si un paramètre est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1a026-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a026-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a026-122">Remarks</span></span>

<span data-ttu-id="1a026-123">La fonction **SzFindSz** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="1a026-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="1a026-124">Recherches dans des formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1a026-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="1a026-125">La longueur maximale sur les deux paramètres est en caractères, pas nécessairement octets.</span><span class="sxs-lookup"><span data-stu-id="1a026-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

