---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libère la mémoire allouée par l'interface IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322056"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="4d1ca-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="4d1ca-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="4d1ca-104">Libère la mémoire allouée par l'interface [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1ca-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4d1ca-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4d1ca-105">Quick info</span></span>

<span data-ttu-id="4d1ca-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="4d1ca-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="4d1ca-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d1ca-107">Parameters</span></span>

<span data-ttu-id="4d1ca-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="4d1ca-108">_pv_</span></span>
  
> <span data-ttu-id="4d1ca-109">dans Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="4d1ca-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4d1ca-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4d1ca-110">Return values</span></span>

<span data-ttu-id="4d1ca-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="4d1ca-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d1ca-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d1ca-112">Remarks</span></span>

<span data-ttu-id="4d1ca-113">Utilisez cette méthode pour libérer de la mémoire allouée par [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="4d1ca-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d1ca-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d1ca-114">See also</span></span>

- [<span data-ttu-id="4d1ca-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="4d1ca-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

