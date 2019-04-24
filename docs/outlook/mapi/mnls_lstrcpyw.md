---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Dernière modification: 18 juin 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341726"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="69755-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="69755-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="69755-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69755-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69755-105">Copie une chaîne dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="69755-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="69755-106">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="69755-106">Do not use.</span></span> <span data-ttu-id="69755-107">EnVisagez d'utiliser [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) à la place.</span><span class="sxs-lookup"><span data-stu-id="69755-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="69755-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69755-108">Parameters</span></span>

<span data-ttu-id="69755-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="69755-109">lpString1</span></span>
  
> <span data-ttu-id="69755-110">remarquer Mémoire tampon pour recevoir le contenu de la chaîne désignée par le paramètre lpString2.</span><span class="sxs-lookup"><span data-stu-id="69755-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="69755-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="69755-111">lpString2</span></span>
  
> <span data-ttu-id="69755-112">dans Chaîne terminée par un caractère null à copier.</span><span class="sxs-lookup"><span data-stu-id="69755-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69755-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69755-113">Return value</span></span>

<span data-ttu-id="69755-114">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="69755-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="69755-115">Si la fonction échoue, la valeur renvoyée est NULL et lpString1 ne peut pas être terminé par null.</span><span class="sxs-lookup"><span data-stu-id="69755-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69755-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="69755-116">Remarks</span></span>

<span data-ttu-id="69755-117">Cette fonction encapsule la fonction **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="69755-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="69755-118">Pour plus d'informations, consultez la rubrique [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="69755-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69755-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69755-119">See also</span></span>



[<span data-ttu-id="69755-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="69755-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

