---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtient une valeur de type String qui représente un identificateur unique de réseau social pour une connexion de réseau social donnée.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433275"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="5dbfb-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="5dbfb-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="5dbfb-104">Obtient une valeur de type String qui représente un identificateur unique de réseau social pour une connexion de réseau social donnée.</span><span class="sxs-lookup"><span data-stu-id="5dbfb-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="5dbfb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dbfb-105">Parameters</span></span>

<span data-ttu-id="5dbfb-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="5dbfb-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="5dbfb-107">remarquer Chaîne qui contient un identificateur unique de réseau social.</span><span class="sxs-lookup"><span data-stu-id="5dbfb-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5dbfb-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dbfb-108">Remarks</span></span>

<span data-ttu-id="5dbfb-109">Un identificateur réseau unique est une chaîne qui identifie le réseau social du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="5dbfb-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="5dbfb-110">Cette méthode peut également renvoyer E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5dbfb-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5dbfb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dbfb-111">See also</span></span>

- [<span data-ttu-id="5dbfb-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5dbfb-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

