---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donné.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787732"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="f08ea-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="f08ea-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="f08ea-104">Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donné.</span><span class="sxs-lookup"><span data-stu-id="f08ea-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="f08ea-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f08ea-105">Parameters</span></span>

<span data-ttu-id="f08ea-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="f08ea-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="f08ea-107">[out] Chaîne qui contient un identificateur unique de réseau social.</span><span class="sxs-lookup"><span data-stu-id="f08ea-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f08ea-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f08ea-108">Remarks</span></span>

<span data-ttu-id="f08ea-109">Un identificateur de réseau unique est une chaîne qui identifie le réseau social du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="f08ea-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="f08ea-110">Cette méthode peut aussi renvoyer E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f08ea-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f08ea-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f08ea-111">See also</span></span>

- [<span data-ttu-id="f08ea-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f08ea-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

