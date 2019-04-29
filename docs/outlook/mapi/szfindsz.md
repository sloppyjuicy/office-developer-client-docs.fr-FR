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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435221"
---
# <a name="szfindsz"></a><span data-ttu-id="b9ad8-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="b9ad8-103">SzFindSz</span></span>

  
  
<span data-ttu-id="b9ad8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9ad8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9ad8-105">Recherche la première occurrence d'une sous-chaîne terminée par un caractère NULL dans une chaîne terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9ad8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b9ad8-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9ad8-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="b9ad8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b9ad8-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b9ad8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9ad8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b9ad8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b9ad8-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b9ad8-110">Called by:</span></span>  <br/> |<span data-ttu-id="b9ad8-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b9ad8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="b9ad8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9ad8-112">Parameters</span></span>

 <span data-ttu-id="b9ad8-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="b9ad8-113">_lpsz_</span></span>
  
> <span data-ttu-id="b9ad8-114">dans Pointeur vers la chaîne terminée par un caractère null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="b9ad8-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="b9ad8-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="b9ad8-116">_lpszKey_</span></span>
  
> <span data-ttu-id="b9ad8-117">dans Pointeur vers la sous-chaîne terminée par un caractère null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="b9ad8-118">Le paramètre _lpszKey_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9ad8-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9ad8-119">Return value</span></span>

 <span data-ttu-id="b9ad8-120">**SzFindSz** renvoie un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="b9ad8-121">Si la sous-chaîne ne se produit nulle part dans la chaîne, si _lpszKey_ est supérieur à _lpsz_, ou si l'un des paramètres est NULL, la valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9ad8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9ad8-122">Remarks</span></span>

<span data-ttu-id="b9ad8-123">La fonction **SzFindSz** recherche une correspondance exacte uniquement; elle est sensible à la casse et aux différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="b9ad8-124">Les recherches dans les formats Unicode et DBCS sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="b9ad8-125">La limite de longueur sur les deux paramètres est exprimée en caractères, pas nécessairement en octets.</span><span class="sxs-lookup"><span data-stu-id="b9ad8-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

