---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782729"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="db64e-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="db64e-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="db64e-104">Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.</span><span class="sxs-lookup"><span data-stu-id="db64e-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db64e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="db64e-105">Quick info</span></span>

<span data-ttu-id="db64e-106">Voir [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="db64e-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="db64e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db64e-107">Parameters</span></span>

<span data-ttu-id="db64e-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="db64e-108">_ppmsess_</span></span>
  
> <span data-ttu-id="db64e-109">[out] La session MAPI en cours.</span><span class="sxs-lookup"><span data-stu-id="db64e-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="db64e-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="db64e-110">Return values</span></span>

<span data-ttu-id="db64e-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="db64e-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db64e-112">Note</span><span class="sxs-lookup"><span data-stu-id="db64e-112">Remarks</span></span>

<span data-ttu-id="db64e-113">En raison de problèmes de référence circulaire, le Gestionnaire de comptes lui-même ne peut pas mettre à jour la référence de la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="db64e-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db64e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db64e-114">See also</span></span>

- [<span data-ttu-id="db64e-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="db64e-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="db64e-116">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db64e-116">IMAPISession : IUnknown</span></span>](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

