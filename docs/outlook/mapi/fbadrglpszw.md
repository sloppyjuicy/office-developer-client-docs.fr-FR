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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565913"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="cc8e8-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="cc8e8-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="cc8e8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc8e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc8e8-105">Valide toutes les chaînes dans un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="cc8e8-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc8e8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cc8e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc8e8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="cc8e8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="cc8e8-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="cc8e8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc8e8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc8e8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc8e8-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="cc8e8-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc8e8-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="cc8e8-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="cc8e8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8e8-112">Parameters</span></span>

 <span data-ttu-id="cc8e8-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="cc8e8-113">_lppszW_</span></span>
  
> <span data-ttu-id="cc8e8-114">[in] Pointeur vers un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="cc8e8-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="cc8e8-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="cc8e8-115">_cStrings_</span></span>
  
> <span data-ttu-id="cc8e8-116">[in] Nombre de chaînes dans le tableau indiqué par le paramètre _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="cc8e8-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc8e8-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="cc8e8-117">Return value</span></span>

<span data-ttu-id="cc8e8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="cc8e8-118">TRUE</span></span> 
  
> <span data-ttu-id="cc8e8-119">Un ou plusieurs des chaînes dans le tableau spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="cc8e8-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="cc8e8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="cc8e8-120">FALSE</span></span> 
  
> <span data-ttu-id="cc8e8-121">Les chaînes dans le tableau spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="cc8e8-121">The strings in the specified array are valid.</span></span>
    

