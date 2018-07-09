---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Dernière modification : 20 février 2012'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784897"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="ad2d3-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="ad2d3-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="ad2d3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad2d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad2d3-105">Vérifie qu’un pointeur vers une chaîne large est valide.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="ad2d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad2d3-106">Parameters</span></span>

 <span data-ttu-id="ad2d3-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ad2d3-107">_lpsz_</span></span>
  
> <span data-ttu-id="ad2d3-108">[in] Pointeur vers la chaîne de caractères large.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="ad2d3-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="ad2d3-109">_ucchMax_</span></span>
  
> <span data-ttu-id="ad2d3-110">[in] La longueur maximale de la chaîne de caractères, y compris la marque de fin.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad2d3-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ad2d3-111">Return value</span></span>

<span data-ttu-id="ad2d3-112">Renvoie une valeur Boolean qui a la valeur true si la chaîne est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad2d3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad2d3-113">Remarks</span></span>

<span data-ttu-id="ad2d3-114">Cette fonction encapsule [IsBadStringPtr](http://msdn.microsoft.com/fr-fr/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad2d3-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/fr-fr/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="ad2d3-115">Pour plus d’informations, voir [IsBadStringPtr](http://msdn.microsoft.com/fr-fr/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad2d3-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/fr-fr/library/aa366714%28VS.85%29.aspx).</span></span>
  

