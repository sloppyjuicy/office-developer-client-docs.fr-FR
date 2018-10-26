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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565913"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="97b47-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="97b47-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="97b47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97b47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97b47-105">Valide toutes les chaînes dans un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="97b47-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b47-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="97b47-106">Header file:</span></span>  <br/> |<span data-ttu-id="97b47-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="97b47-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="97b47-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="97b47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="97b47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="97b47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="97b47-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="97b47-110">Called by:</span></span>  <br/> |<span data-ttu-id="97b47-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="97b47-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="97b47-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97b47-112">Parameters</span></span>

 <span data-ttu-id="97b47-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="97b47-113">_lppszW_</span></span>
  
> <span data-ttu-id="97b47-114">[in] Pointeur vers un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="97b47-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="97b47-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="97b47-115">_cStrings_</span></span>
  
> <span data-ttu-id="97b47-116">[in] Nombre de chaînes dans le tableau indiqué par le paramètre _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="97b47-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97b47-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="97b47-117">Return value</span></span>

<span data-ttu-id="97b47-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="97b47-118">TRUE</span></span> 
  
> <span data-ttu-id="97b47-119">Un ou plusieurs des chaînes dans le tableau spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="97b47-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="97b47-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="97b47-120">FALSE</span></span> 
  
> <span data-ttu-id="97b47-121">Les chaînes dans le tableau spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="97b47-121">The strings in the specified array are valid.</span></span>
    

