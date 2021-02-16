---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338464"
---
# <a name="mnls_lstrlenw"></a><span data-ttu-id="c2968-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="c2968-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="c2968-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2968-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2968-105">Détermine la longueur de la chaîne Unicode spécifiée, à l’exception du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c2968-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="c2968-106">Envisagez plutôt [d’utiliser StringCchLength.](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2968-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="c2968-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2968-107">Parameters</span></span>

 <span data-ttu-id="c2968-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="c2968-108">_lpsz_</span></span>
  
> <span data-ttu-id="c2968-109">[in] Chaîne Unicode terminée par null à vérifier.</span><span class="sxs-lookup"><span data-stu-id="c2968-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2968-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2968-110">Return value</span></span>

<span data-ttu-id="c2968-111">La fonction renvoie un nombre integer avec la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c2968-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="c2968-112">Il s’agit d’un nombre de caractères dans la chaîne, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c2968-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="c2968-113">Si  _lpsz est_ NULL, la fonction renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="c2968-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2968-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2968-114">Remarks</span></span>

<span data-ttu-id="c2968-115">Cette fonction encapsule **la fonction lstrlen.**</span><span class="sxs-lookup"><span data-stu-id="c2968-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="c2968-116">Pour plus d’informations, voir [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2968-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2968-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2968-117">See also</span></span>



[<span data-ttu-id="c2968-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="c2968-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="c2968-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="c2968-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

