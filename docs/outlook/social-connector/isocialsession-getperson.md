---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtient une interface ISocialPerson basée sur le paramètre userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439820"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="0f2bc-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="0f2bc-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="0f2bc-104">Obtient une interface [ISocialPerson](isocialpersoniunknown.md) basée sur le paramètre _userid_ .</span><span class="sxs-lookup"><span data-stu-id="0f2bc-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="0f2bc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f2bc-105">Parameters</span></span>

<span data-ttu-id="0f2bc-106">_Identifi_</span><span class="sxs-lookup"><span data-stu-id="0f2bc-106">_userId_</span></span>
  
> <span data-ttu-id="0f2bc-107">dans Chaîne qui contient un ID d'utilisateur ou une adresse SMTP d'une personne.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="0f2bc-108">_result_</span><span class="sxs-lookup"><span data-stu-id="0f2bc-108">_result_</span></span>
  
> <span data-ttu-id="0f2bc-109">remarquer Une interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="0f2bc-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0f2bc-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f2bc-110">Remarks</span></span>

<span data-ttu-id="0f2bc-111">Le paramètre _userid_ doit être un ID d'utilisateur ou une adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f2bc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f2bc-112">See also</span></span>

- [<span data-ttu-id="0f2bc-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f2bc-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

