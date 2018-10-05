---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388902"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="659bb-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="659bb-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="659bb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="659bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="659bb-105">Vérifie que le processus appelant dispose d’un accès en lecture à la plage spécifiée de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="659bb-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="659bb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="659bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="659bb-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="659bb-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="659bb-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="659bb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="659bb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="659bb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="659bb-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="659bb-110">Called by:</span></span>  <br/> |<span data-ttu-id="659bb-111">Applications clientes et des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="659bb-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="659bb-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="659bb-112">Parameters</span></span>

 <span data-ttu-id="659bb-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="659bb-113">_lpsz_</span></span>
  
> <span data-ttu-id="659bb-114">[in] Pointeur vers une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="659bb-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="659bb-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="659bb-115">_cchMax_</span></span>
  
> <span data-ttu-id="659bb-116">[in] La taille maximale de la chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="659bb-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="659bb-117">La fonction vérifie l’accès en lecture dans tous les caractères jusqu'à le caractère null de fin de la chaîne, ou le nombre de caractères spécifié par ce paramètre, la plus petite.</span><span class="sxs-lookup"><span data-stu-id="659bb-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="659bb-118">Si ce paramètre est zéro, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="659bb-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="659bb-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="659bb-119">Return value</span></span>

<span data-ttu-id="659bb-120">La valeur de retour est égale à zéro lorsque le processus d’appel a accès en lecture à tous les caractères jusqu'à le caractère null de fin de la chaîne ou le nombre de caractères spécifié par _cchMax_un accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="659bb-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="659bb-121">La valeur de retour est différent de zéro lorsque le processus appelant ne dispose pas d’un accès en lecture à tous les caractères jusqu'à le caractère null de fin de la chaîne ou le nombre de caractères spécifié par _cchMax_un accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="659bb-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="659bb-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="659bb-122">Remarks</span></span>

<span data-ttu-id="659bb-123">La fonction **IsBadBoundedStringPtr** est équivalente à l’aide de **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="659bb-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="659bb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="659bb-124">See also</span></span>



[<span data-ttu-id="659bb-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="659bb-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

