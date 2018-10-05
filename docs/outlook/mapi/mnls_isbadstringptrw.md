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
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398737"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="01a81-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="01a81-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="01a81-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01a81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01a81-105">Vérifie qu’un pointeur vers une chaîne large est valide.</span><span class="sxs-lookup"><span data-stu-id="01a81-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="01a81-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01a81-106">Parameters</span></span>

 <span data-ttu-id="01a81-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="01a81-107">_lpsz_</span></span>
  
> <span data-ttu-id="01a81-108">[in] Pointeur vers la chaîne de caractères large.</span><span class="sxs-lookup"><span data-stu-id="01a81-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="01a81-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="01a81-109">_ucchMax_</span></span>
  
> <span data-ttu-id="01a81-110">[in] La longueur maximale de la chaîne de caractères, y compris la marque de fin.</span><span class="sxs-lookup"><span data-stu-id="01a81-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01a81-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01a81-111">Return value</span></span>

<span data-ttu-id="01a81-112">Renvoie une valeur Boolean qui a la valeur true si la chaîne est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="01a81-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01a81-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="01a81-113">Remarks</span></span>

<span data-ttu-id="01a81-114">Cette fonction encapsule [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="01a81-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="01a81-115">Pour plus d’informations, voir [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="01a81-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

