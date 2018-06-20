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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787324"
---
# <a name="szfindsz"></a><span data-ttu-id="f7e65-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="f7e65-103">SzFindSz</span></span>

  
  
<span data-ttu-id="f7e65-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7e65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7e65-105">Recherche la première occurrence d’une sous-chaîne terminée dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f7e65-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7e65-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f7e65-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7e65-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f7e65-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f7e65-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="f7e65-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7e65-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7e65-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7e65-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="f7e65-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7e65-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f7e65-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="f7e65-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7e65-112">Parameters</span></span>

 <span data-ttu-id="f7e65-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="f7e65-113">_lpsz_</span></span>
  
> <span data-ttu-id="f7e65-114">[in] Pointeur vers la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="f7e65-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="f7e65-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="f7e65-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="f7e65-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="f7e65-116">_lpszKey_</span></span>
  
> <span data-ttu-id="f7e65-117">[in] Pointeur vers la sous-chaîne terminée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="f7e65-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="f7e65-118">Le paramètre _lpszKey_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="f7e65-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7e65-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f7e65-119">Return value</span></span>

 <span data-ttu-id="f7e65-120">**SzFindSz** retourne un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f7e65-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="f7e65-121">Si la sous-chaîne ne se produit pas n’importe où dans la chaîne, si _lpszKey_ est supérieure à _lpsz_, ou si un paramètre est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f7e65-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7e65-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7e65-122">Remarks</span></span>

<span data-ttu-id="f7e65-123">La fonction **SzFindSz** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="f7e65-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="f7e65-124">Recherches dans des formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f7e65-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="f7e65-125">La longueur maximale sur les deux paramètres est en caractères, pas nécessairement octets.</span><span class="sxs-lookup"><span data-stu-id="f7e65-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

