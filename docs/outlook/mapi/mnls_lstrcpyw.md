---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Dernière modification : 18 juin 2012'
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784903"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="1a205-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="1a205-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="1a205-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a205-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a205-105">Copie une chaîne dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1a205-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="1a205-106">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="1a205-106">Do not use.</span></span> <span data-ttu-id="1a205-107">Utilisez plutôt [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1a205-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="1a205-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a205-108">Parameters</span></span>

<span data-ttu-id="1a205-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="1a205-109">lpString1</span></span>
  
> <span data-ttu-id="1a205-110">[out] Mémoire tampon pour recevoir le contenu de la chaîne indiquée par le paramètre lpString2.</span><span class="sxs-lookup"><span data-stu-id="1a205-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="1a205-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="1a205-111">lpString2</span></span>
  
> <span data-ttu-id="1a205-112">[in] La chaîne à copier.</span><span class="sxs-lookup"><span data-stu-id="1a205-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a205-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1a205-113">Return value</span></span>

<span data-ttu-id="1a205-114">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1a205-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="1a205-115">Si la fonction échoue, la valeur de retour est NULL et lpString1 ne peut pas être terminée.</span><span class="sxs-lookup"><span data-stu-id="1a205-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a205-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a205-116">Remarks</span></span>

<span data-ttu-id="1a205-117">Cette fonction encapsule la fonction **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="1a205-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="1a205-118">Pour plus d’informations, voir [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a205-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a205-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a205-119">See also</span></span>



[<span data-ttu-id="1a205-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="1a205-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

