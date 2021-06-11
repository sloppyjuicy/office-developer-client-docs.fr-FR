---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Renvoie une chaîne qui représente le nom du réseau social.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406877"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="a714e-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="a714e-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="a714e-104">Renvoie une chaîne qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="a714e-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="a714e-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a714e-105">Property value</span></span>

<span data-ttu-id="a714e-106">Chaîne qui contient le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="a714e-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a714e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a714e-107">Remarks</span></span>

<span data-ttu-id="a714e-108">Outlook Les fournisseurs OSC (Social Connector) doivent localiser le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="a714e-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a714e-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a714e-109">See also</span></span>

- [<span data-ttu-id="a714e-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a714e-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

