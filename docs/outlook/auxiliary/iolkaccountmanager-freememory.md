---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libère la mémoire allouée par l’interface IOlkAccountManager.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782710"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="6d74e-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="6d74e-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="6d74e-104">Libère la mémoire allouée par l’interface [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="6d74e-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6d74e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="6d74e-105">Quick info</span></span>

<span data-ttu-id="6d74e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="6d74e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="6d74e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d74e-107">Parameters</span></span>

<span data-ttu-id="6d74e-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="6d74e-108">_pv_</span></span>
  
> <span data-ttu-id="6d74e-109">[in] Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="6d74e-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6d74e-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="6d74e-110">Return values</span></span>

<span data-ttu-id="6d74e-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="6d74e-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d74e-112">Note</span><span class="sxs-lookup"><span data-stu-id="6d74e-112">Remarks</span></span>

<span data-ttu-id="6d74e-113">Utilisez cette méthode pour libérer de la mémoire allouée par [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="6d74e-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d74e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d74e-114">See also</span></span>

- [<span data-ttu-id="6d74e-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="6d74e-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

