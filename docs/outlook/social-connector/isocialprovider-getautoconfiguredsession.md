---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Récupère une interface ISocialSession configurée automatiquement.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285778"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="f21b0-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="f21b0-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="f21b0-104">Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f21b0-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="f21b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f21b0-105">Parameters</span></span>

<span data-ttu-id="f21b0-106">_session_</span><span class="sxs-lookup"><span data-stu-id="f21b0-106">_session_</span></span>
  
> <span data-ttu-id="f21b0-107">[out] Une interface **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="f21b0-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f21b0-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f21b0-108">Remarks</span></span>

<span data-ttu-id="f21b0-109">L’interface **ISocialSession** renvoyée est automatiquement connectée au réseau, selon une méthode propre au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f21b0-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="f21b0-110">Le fournisseur doit renvoyer l’erreur OSC_E_NOT_IMPLEMENTED si le réseau social ne prend pas en charge la configuration automatique.</span><span class="sxs-lookup"><span data-stu-id="f21b0-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="f21b0-111">Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f21b0-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f21b0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f21b0-112">See also</span></span>

- [<span data-ttu-id="f21b0-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f21b0-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

