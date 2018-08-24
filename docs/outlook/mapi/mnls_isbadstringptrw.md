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
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589566"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="b7897-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="b7897-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="b7897-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7897-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7897-105">Vérifie qu’un pointeur vers une chaîne large est valide.</span><span class="sxs-lookup"><span data-stu-id="b7897-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="b7897-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7897-106">Parameters</span></span>

 <span data-ttu-id="b7897-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="b7897-107">_lpsz_</span></span>
  
> <span data-ttu-id="b7897-108">[in] Pointeur vers la chaîne de caractères large.</span><span class="sxs-lookup"><span data-stu-id="b7897-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="b7897-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="b7897-109">_ucchMax_</span></span>
  
> <span data-ttu-id="b7897-110">[in] La longueur maximale de la chaîne de caractères, y compris la marque de fin.</span><span class="sxs-lookup"><span data-stu-id="b7897-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7897-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b7897-111">Return value</span></span>

<span data-ttu-id="b7897-112">Renvoie une valeur Boolean qui a la valeur true si la chaîne est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="b7897-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7897-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7897-113">Remarks</span></span>

<span data-ttu-id="b7897-114">Cette fonction encapsule [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7897-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="b7897-115">Pour plus d’informations, voir [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7897-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

