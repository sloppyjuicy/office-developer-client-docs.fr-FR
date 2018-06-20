---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtient une interface ISocialPerson en fonction du paramètre userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787608"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="4a38d-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="4a38d-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="4a38d-104">Obtient une interface [ISocialPerson](isocialpersoniunknown.md) en fonction du paramètre _userID_ .</span><span class="sxs-lookup"><span data-stu-id="4a38d-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="4a38d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a38d-105">Parameters</span></span>

<span data-ttu-id="4a38d-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="4a38d-106">_userId_</span></span>
  
> <span data-ttu-id="4a38d-107">[in] Chaîne qui contient une utilisateur ID ou une adresse SMTP d’une personne.</span><span class="sxs-lookup"><span data-stu-id="4a38d-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="4a38d-108">_résultat_</span><span class="sxs-lookup"><span data-stu-id="4a38d-108">_result_</span></span>
  
> <span data-ttu-id="4a38d-109">[out] Une interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="4a38d-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a38d-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a38d-110">Remarks</span></span>

<span data-ttu-id="4a38d-111">Le paramètre _userID_ doit être une utilisateur ID ou une adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="4a38d-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a38d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a38d-112">See also</span></span>

- [<span data-ttu-id="4a38d-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a38d-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

