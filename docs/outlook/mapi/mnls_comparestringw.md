---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Dernière modification : 20 février 2012'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576175"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="0d804-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="0d804-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="0d804-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d804-105">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d804-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="0d804-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d804-106">Parameters</span></span>

 <span data-ttu-id="0d804-107">_LCID_</span><span class="sxs-lookup"><span data-stu-id="0d804-107">_lcid_</span></span>
  
> <span data-ttu-id="0d804-108">[in] Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0d804-108">[in] Locale identifier.</span></span> <span data-ttu-id="0d804-109">Pour les définitions détaillées, voir le paramètre _Locale_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d804-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="0d804-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="0d804-110">_dwFlags_</span></span>
  
> <span data-ttu-id="0d804-111">[in] Indicateurs à ignorer la casse et des signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="0d804-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="0d804-112">Pour les définitions détaillées, voir le paramètre _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d804-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="0d804-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="0d804-113">_pstr1_</span></span>
  
> <span data-ttu-id="0d804-114">[in] Pointeur vers la première chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="0d804-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="0d804-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="0d804-115">_cch1_</span></span>
  
> <span data-ttu-id="0d804-116">[in] Longueur en caractères de la première chaîne Unicode, à l’exception du caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="0d804-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="0d804-117">L’application peut fournir une valeur négative si la chaîne est terminée.</span><span class="sxs-lookup"><span data-stu-id="0d804-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="0d804-118">Dans ce cas, la fonction **MNLS_CompareStringW** détermine automatiquement la longueur.</span><span class="sxs-lookup"><span data-stu-id="0d804-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="0d804-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="0d804-119">_pstr2_</span></span>
  
> <span data-ttu-id="0d804-120">[in] Pointeur vers la deuxième chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="0d804-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="0d804-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="0d804-121">_cch2_</span></span>
  
> <span data-ttu-id="0d804-122">[in] Longueur en caractères de la deuxième chaîne Unicode, à l’exception du caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="0d804-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="0d804-123">L’application peut fournir une valeur négative si la chaîne est terminée.</span><span class="sxs-lookup"><span data-stu-id="0d804-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="0d804-124">Dans ce cas, la fonction détermine automatiquement la longueur.</span><span class="sxs-lookup"><span data-stu-id="0d804-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d804-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0d804-125">Return value</span></span>

<span data-ttu-id="0d804-126">Renvoie les valeurs indiquées pour [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d804-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d804-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d804-127">Remarks</span></span>

<span data-ttu-id="0d804-128">Cette fonction encapsule [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d804-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="0d804-129">**MNLS_CompareStringW** accepte les mêmes paramètres et a le même comportement que [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d804-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d804-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d804-130">See also</span></span>



[<span data-ttu-id="0d804-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="0d804-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="0d804-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="0d804-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

