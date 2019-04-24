---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278833"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="e09d6-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="e09d6-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="e09d6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e09d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e09d6-105">Vérifie que le processus appelant dispose d'un accès en lecture à la plage de mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e09d6-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e09d6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e09d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="e09d6-107">mapiwin. h</span><span class="sxs-lookup"><span data-stu-id="e09d6-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="e09d6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e09d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e09d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e09d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e09d6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e09d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="e09d6-111">Applications clientes et fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="e09d6-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="e09d6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e09d6-112">Parameters</span></span>

 <span data-ttu-id="e09d6-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e09d6-113">_lpsz_</span></span>
  
> <span data-ttu-id="e09d6-114">dans Pointeur vers une chaîne ASCII terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="e09d6-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="e09d6-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="e09d6-115">_cchMax_</span></span>
  
> <span data-ttu-id="e09d6-116">dans Taille maximale de la chaîne, en caractères.</span><span class="sxs-lookup"><span data-stu-id="e09d6-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="e09d6-117">La fonction vérifie l'accès en lecture dans tous les caractères jusqu'au caractère null de fin de la chaîne, ou jusqu'au nombre de caractères spécifiés par ce paramètre, la valeur la plus petite étant retenue.</span><span class="sxs-lookup"><span data-stu-id="e09d6-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="e09d6-118">Si ce paramètre est égal à zéro, la valeur renvoyée est zéro.</span><span class="sxs-lookup"><span data-stu-id="e09d6-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e09d6-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e09d6-119">Return value</span></span>

<span data-ttu-id="e09d6-120">La valeur renvoyée est zéro lorsque le processus appelant a accès en lecture à tous les caractères jusqu'au caractère null de fin de la chaîne ou accès en lecture au nombre de caractères spécifié par _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="e09d6-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="e09d6-121">La valeur renvoyée est différente de zéro lorsque le processus appelant n'a pas accès en lecture à tous les caractères jusqu'au caractère null de fin de la chaîne, ou accès en lecture maximum au nombre de caractères spécifié par _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="e09d6-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e09d6-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="e09d6-122">Remarks</span></span>

<span data-ttu-id="e09d6-123">La fonction **IsBadBoundedStringPtr** est équivalente à l'utilisation de **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="e09d6-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e09d6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e09d6-124">See also</span></span>



[<span data-ttu-id="e09d6-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="e09d6-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

