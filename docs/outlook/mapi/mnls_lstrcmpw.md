---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Dernière modification : 18 juin 2012'
ms.openlocfilehash: 36e22c60b32242425335b122b66c2c77e376848b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580116"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="a7c10-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="a7c10-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="a7c10-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7c10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7c10-105">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="a7c10-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="a7c10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7c10-106">Parameters</span></span>

 <span data-ttu-id="a7c10-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="a7c10-107">_lpString1_</span></span>
  
> <span data-ttu-id="a7c10-108">[in] Pointeur vers la première chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="a7c10-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="a7c10-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="a7c10-109">_lpString2_</span></span>
  
> <span data-ttu-id="a7c10-110">[in] Pointeur vers la deuxième chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="a7c10-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7c10-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a7c10-111">Return value</span></span>

<span data-ttu-id="a7c10-112">Renvoie les valeurs décrites pour un appel à **MNLS_CompareStringW** à l’exception de CSTR_EQUAL équivalent.</span><span class="sxs-lookup"><span data-stu-id="a7c10-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a7c10-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7c10-113">Remarks</span></span>

 <span data-ttu-id="a7c10-114">_MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux de GetUserDefaultLCID, 0 pour les indicateurs et -1 pour cch1 et cch2.</span><span class="sxs-lookup"><span data-stu-id="a7c10-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7c10-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7c10-115">See also</span></span>



[<span data-ttu-id="a7c10-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="a7c10-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

