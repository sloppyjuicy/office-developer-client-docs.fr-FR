---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356839"
---
# <a name="mnls_lstrcmpw"></a><span data-ttu-id="6db9a-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="6db9a-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="6db9a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6db9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6db9a-105">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="6db9a-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="6db9a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6db9a-106">Parameters</span></span>

 <span data-ttu-id="6db9a-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="6db9a-107">_lpString1_</span></span>
  
> <span data-ttu-id="6db9a-108">[in] Pointeur vers la première chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="6db9a-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="6db9a-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="6db9a-109">_lpString2_</span></span>
  
> <span data-ttu-id="6db9a-110">[in] Pointeur vers la deuxième chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="6db9a-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6db9a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6db9a-111">Return value</span></span>

<span data-ttu-id="6db9a-112">Renvoie les valeurs décrites pour un appel équivalent **à MNLS_CompareStringW** à l’exception de CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="6db9a-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6db9a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="6db9a-113">Remarks</span></span>

 <span data-ttu-id="6db9a-114">_MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux GetUserDefaultLCID, 0 pour les indicateurs et -1 pour cch1 et cch2.</span><span class="sxs-lookup"><span data-stu-id="6db9a-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6db9a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db9a-115">See also</span></span>



[<span data-ttu-id="6db9a-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="6db9a-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

