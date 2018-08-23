---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570876"
---
# <a name="szfindlastch"></a><span data-ttu-id="4b210-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="4b210-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="4b210-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b210-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b210-105">Recherche la dernière occurrence d’un caractère dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4b210-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b210-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4b210-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b210-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b210-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b210-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4b210-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4b210-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4b210-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4b210-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4b210-110">Called by:</span></span>  <br/> |<span data-ttu-id="4b210-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4b210-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="4b210-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b210-112">Parameters</span></span>

 <span data-ttu-id="4b210-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="4b210-113">_lpsz_</span></span>
  
> <span data-ttu-id="4b210-114">[in] Pointeur vers la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="4b210-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="4b210-115">_CH_</span><span class="sxs-lookup"><span data-stu-id="4b210-115">_ch_</span></span>
  
> <span data-ttu-id="4b210-116">[in] Le caractère à rechercher.</span><span class="sxs-lookup"><span data-stu-id="4b210-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b210-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4b210-117">Return value</span></span>

 <span data-ttu-id="4b210-118">**SzFindLastCh** retourne un pointeur vers la dernière occurrence du caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4b210-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="4b210-119">Si le caractère ne se produit pas n’importe où dans la chaîne, ou si le paramètre _lpsz_ est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="4b210-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4b210-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b210-120">Remarks</span></span>

<span data-ttu-id="4b210-121">La fonction **SzFindLastCh** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="4b210-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="4b210-122">Recherches dans les formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4b210-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

