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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341054"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="b098c-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="b098c-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="b098c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b098c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b098c-105">Valide toutes les chaînes dans un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="b098c-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b098c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b098c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b098c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b098c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b098c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b098c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b098c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b098c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b098c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b098c-110">Called by:</span></span>  <br/> |<span data-ttu-id="b098c-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b098c-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="b098c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b098c-112">Parameters</span></span>

 <span data-ttu-id="b098c-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="b098c-113">_lppszW_</span></span>
  
> <span data-ttu-id="b098c-114">dans Pointeur vers un tableau de chaînes Unicode terminées par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="b098c-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="b098c-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="b098c-115">_cStrings_</span></span>
  
> <span data-ttu-id="b098c-116">dans Nombre de chaînes dans le tableau vers lequel pointe le paramètre _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="b098c-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b098c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b098c-117">Return value</span></span>

<span data-ttu-id="b098c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="b098c-118">TRUE</span></span> 
  
> <span data-ttu-id="b098c-119">Une ou plusieurs des chaînes du tableau spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="b098c-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="b098c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="b098c-120">FALSE</span></span> 
  
> <span data-ttu-id="b098c-121">Les chaînes du tableau spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="b098c-121">The strings in the specified array are valid.</span></span>
    

