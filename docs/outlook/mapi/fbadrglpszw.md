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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783282"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="59bde-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="59bde-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="59bde-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59bde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59bde-105">Valide toutes les chaînes dans un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="59bde-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59bde-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="59bde-106">Header file:</span></span>  <br/> |<span data-ttu-id="59bde-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="59bde-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="59bde-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="59bde-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="59bde-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="59bde-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="59bde-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="59bde-110">Called by:</span></span>  <br/> |<span data-ttu-id="59bde-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="59bde-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="59bde-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59bde-112">Parameters</span></span>

 <span data-ttu-id="59bde-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="59bde-113">_lppszW_</span></span>
  
> <span data-ttu-id="59bde-114">[in] Pointeur vers un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="59bde-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="59bde-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="59bde-115">_cStrings_</span></span>
  
> <span data-ttu-id="59bde-116">[in] Nombre de chaînes dans le tableau indiqué par le paramètre _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="59bde-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="59bde-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="59bde-117">Return value</span></span>

<span data-ttu-id="59bde-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="59bde-118">TRUE</span></span> 
  
> <span data-ttu-id="59bde-119">Un ou plusieurs des chaînes dans le tableau spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="59bde-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="59bde-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="59bde-120">FALSE</span></span> 
  
> <span data-ttu-id="59bde-121">Les chaînes dans le tableau spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="59bde-121">The strings in the specified array are valid.</span></span>
    

