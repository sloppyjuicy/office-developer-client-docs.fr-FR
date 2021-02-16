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
# <a name="szfindsz"></a><span data-ttu-id="62c78-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="62c78-103">SzFindSz</span></span>

  
  
<span data-ttu-id="62c78-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62c78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62c78-105">Recherche la première occurrence d’une sous-chaîne terminée par null dans une chaîne terminée par null.</span><span class="sxs-lookup"><span data-stu-id="62c78-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62c78-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="62c78-106">Header file:</span></span>  <br/> |<span data-ttu-id="62c78-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="62c78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="62c78-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="62c78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="62c78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="62c78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="62c78-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="62c78-110">Called by:</span></span>  <br/> |<span data-ttu-id="62c78-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="62c78-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="62c78-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62c78-112">Parameters</span></span>

 <span data-ttu-id="62c78-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="62c78-113">_lpsz_</span></span>
  
> <span data-ttu-id="62c78-114">[in] Pointeur vers la chaîne terminée par null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="62c78-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="62c78-115">Le  _paramètre lpsz_ ne doit pas dépasser 65 536 caractères.</span><span class="sxs-lookup"><span data-stu-id="62c78-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="62c78-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="62c78-116">_lpszKey_</span></span>
  
> <span data-ttu-id="62c78-117">[in] Pointeur vers la sous-stration terminée par null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="62c78-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="62c78-118">Le  _paramètre lpszKey_ ne doit pas dépasser 65 536 caractères.</span><span class="sxs-lookup"><span data-stu-id="62c78-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="62c78-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62c78-119">Return value</span></span>

 <span data-ttu-id="62c78-120">**SzFindSz** renvoie un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="62c78-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="62c78-121">Si la sous-chaîne ne se produit pas dans la chaîne, si  _lpszKey_ est supérieur à  _lpsz_ ou si l’un des paramètres est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="62c78-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="62c78-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="62c78-122">Remarks</span></span>

<span data-ttu-id="62c78-123">La **fonction SzFindSz** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas.</span><span class="sxs-lookup"><span data-stu-id="62c78-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="62c78-124">Les recherches au format Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62c78-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="62c78-125">La limite de longueur pour les deux paramètres est en caractères, pas nécessairement en octets.</span><span class="sxs-lookup"><span data-stu-id="62c78-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

