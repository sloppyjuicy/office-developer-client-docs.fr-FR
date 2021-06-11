---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356846"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="c3d67-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="c3d67-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="c3d67-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d67-105">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3d67-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="c3d67-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c3d67-106">Parameters</span></span>

 <span data-ttu-id="c3d67-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="c3d67-107">_lcid_</span></span>
  
> <span data-ttu-id="c3d67-108">[in] Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="c3d67-108">[in] Locale identifier.</span></span> <span data-ttu-id="c3d67-109">Pour obtenir des définitions détaillées, voir le paramètre  _Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3d67-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="c3d67-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="c3d67-110">_dwFlags_</span></span>
  
> <span data-ttu-id="c3d67-111">[in] Indicateurs pour ignorer la case et les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="c3d67-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="c3d67-112">Pour obtenir des définitions détaillées, voir le  _paramètre dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3d67-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="c3d67-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="c3d67-113">_pstr1_</span></span>
  
> <span data-ttu-id="c3d67-114">[in] Pointeur vers la première chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="c3d67-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="c3d67-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="c3d67-115">_cch1_</span></span>
  
> <span data-ttu-id="c3d67-116">[in] Longueur en caractères de la première chaîne Unicode, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c3d67-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="c3d67-117">L’application peut fournir une valeur négative si la chaîne est terminée par null.</span><span class="sxs-lookup"><span data-stu-id="c3d67-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="c3d67-118">Dans ce cas, la **fonction MNLS_CompareStringW** détermine automatiquement la longueur.</span><span class="sxs-lookup"><span data-stu-id="c3d67-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="c3d67-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="c3d67-119">_pstr2_</span></span>
  
> <span data-ttu-id="c3d67-120">[in] Pointeur vers la deuxième chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="c3d67-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="c3d67-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="c3d67-121">_cch2_</span></span>
  
> <span data-ttu-id="c3d67-122">[in] Longueur en caractères de la deuxième chaîne Unicode, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c3d67-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="c3d67-123">L’application peut fournir une valeur négative si la chaîne est terminée par null.</span><span class="sxs-lookup"><span data-stu-id="c3d67-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="c3d67-124">Dans ce cas, la fonction détermine automatiquement la longueur.</span><span class="sxs-lookup"><span data-stu-id="c3d67-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c3d67-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c3d67-125">Return value</span></span>

<span data-ttu-id="c3d67-126">Renvoie les valeurs décrites [pour CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3d67-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3d67-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="c3d67-127">Remarks</span></span>

<span data-ttu-id="c3d67-128">Cette fonction [encapsule CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3d67-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="c3d67-129">**MNLS_CompareStringW** prend les mêmes paramètres et a le même comportement que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3d67-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3d67-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d67-130">See also</span></span>



[<span data-ttu-id="c3d67-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="c3d67-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="c3d67-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="c3d67-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

