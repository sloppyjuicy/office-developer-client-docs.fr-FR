---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libère la mémoire allouée par l'interface IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321335"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="fb58e-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="fb58e-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="fb58e-104">Libère la mémoire allouée par l'interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="fb58e-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fb58e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fb58e-105">Quick info</span></span>

<span data-ttu-id="fb58e-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="fb58e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="fb58e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb58e-107">Parameters</span></span>

<span data-ttu-id="fb58e-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="fb58e-108">_pv_</span></span>
  
> <span data-ttu-id="fb58e-109">dans Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="fb58e-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fb58e-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="fb58e-110">Return values</span></span>

<span data-ttu-id="fb58e-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fb58e-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb58e-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb58e-112">Remarks</span></span>

<span data-ttu-id="fb58e-113">Utilisez cette méthode pour libérer de la mémoire allouée par [IOlkAccount:: getprop](iolkaccount-getprop.md) (si la valeur de la propriété Account spécifiée est un type binaire ou String) et [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="fb58e-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb58e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb58e-114">See also</span></span>

- [<span data-ttu-id="fb58e-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fb58e-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="fb58e-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="fb58e-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

