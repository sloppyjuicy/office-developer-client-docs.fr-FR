---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Dernière modification : 21 février 2012'
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588887"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="dfe1b-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="dfe1b-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="dfe1b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfe1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfe1b-105">Détermine la longueur de la chaîne Unicode spécifiée, à l’exception du caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="dfe1b-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="dfe1b-106">Utilisez plutôt [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dfe1b-106">Consider using [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="dfe1b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfe1b-107">Parameters</span></span>

 <span data-ttu-id="dfe1b-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="dfe1b-108">_lpsz_</span></span>
  
> <span data-ttu-id="dfe1b-109">[in] La chaîne Unicode terminée par null à vérifier.</span><span class="sxs-lookup"><span data-stu-id="dfe1b-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfe1b-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dfe1b-110">Return value</span></span>

<span data-ttu-id="dfe1b-111">La fonction retourne un entier avec la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="dfe1b-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="dfe1b-112">Il s’agit d’un nombre de caractères dans la chaîne, à l’exception du caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="dfe1b-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="dfe1b-113">Si _lpsz_ est NULL, la fonction renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="dfe1b-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dfe1b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dfe1b-114">Remarks</span></span>

<span data-ttu-id="dfe1b-115">Cette fonction à la ligne de la fonction **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="dfe1b-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="dfe1b-116">Pour plus d’informations, voir [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dfe1b-116">For more information, see [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dfe1b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfe1b-117">See also</span></span>



[<span data-ttu-id="dfe1b-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="dfe1b-118">lstrlen</span></span>](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="dfe1b-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="dfe1b-119">StringCchLength</span></span>](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

