---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421941"
---
# <a name="szfindch"></a><span data-ttu-id="e224f-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="e224f-103">SzFindCh</span></span>
 
<span data-ttu-id="e224f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e224f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e224f-105">Recherche la première occurrence d’un caractère dans une chaîne terminée par null.</span><span class="sxs-lookup"><span data-stu-id="e224f-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e224f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e224f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e224f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e224f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e224f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e224f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e224f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e224f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e224f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e224f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e224f-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e224f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="e224f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e224f-112">Parameters</span></span>

<span data-ttu-id="e224f-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e224f-113">_lpsz_</span></span>
  
> <span data-ttu-id="e224f-114">[in] Pointeur vers la chaîne terminée par null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="e224f-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="e224f-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="e224f-115">_ch_</span></span>
  
> <span data-ttu-id="e224f-116">[in] Caractère à rechercher.</span><span class="sxs-lookup"><span data-stu-id="e224f-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e224f-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e224f-117">Return value</span></span>

<span data-ttu-id="e224f-118">**SzFindCh renvoie** un pointeur vers la première occurrence du caractère dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e224f-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="e224f-119">Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre  _lpsz_ est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e224f-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e224f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="e224f-120">Remarks</span></span>

<span data-ttu-id="e224f-121">La **fonction SzFindCh** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas.</span><span class="sxs-lookup"><span data-stu-id="e224f-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="e224f-122">Les recherches dans les formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e224f-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

