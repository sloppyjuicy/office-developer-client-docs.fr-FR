---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436439"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="2ebe7-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="2ebe7-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="2ebe7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ebe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ebe7-105">Valide toutes les chaînes d’un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ebe7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2ebe7-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ebe7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2ebe7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2ebe7-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2ebe7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ebe7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ebe7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ebe7-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2ebe7-110">Called by:</span></span>  <br/> |<span data-ttu-id="2ebe7-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="2ebe7-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="2ebe7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ebe7-112">Parameters</span></span>

 <span data-ttu-id="2ebe7-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="2ebe7-113">_lppszW_</span></span>
  
> <span data-ttu-id="2ebe7-114">[in] Pointeur vers un tableau de chaînes Unicode terminées par null.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="2ebe7-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="2ebe7-115">_cStrings_</span></span>
  
> <span data-ttu-id="2ebe7-116">[in] Nombre de chaînes dans le tableau pointées par _le paramètre lppszW._</span><span class="sxs-lookup"><span data-stu-id="2ebe7-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ebe7-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2ebe7-117">Return value</span></span>

<span data-ttu-id="2ebe7-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ebe7-118">TRUE</span></span> 
  
> <span data-ttu-id="2ebe7-119">Une ou plusieurs des chaînes du tableau spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="2ebe7-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="2ebe7-120">FALSE</span></span> 
  
> <span data-ttu-id="2ebe7-121">Les chaînes du tableau spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-121">The strings in the specified array are valid.</span></span>
    

