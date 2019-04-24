---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Renvoie une valeur de type String qui représente le nom du réseau social.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285490"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="c6601-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="c6601-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="c6601-104">Renvoie une valeur de type String qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="c6601-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="c6601-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c6601-105">Property value</span></span>

<span data-ttu-id="c6601-106">Chaîne qui contient le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="c6601-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6601-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6601-107">Remarks</span></span>

<span data-ttu-id="c6601-108">Les fournisseurs Outlook Social Connector (OSC) doivent localiser le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="c6601-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6601-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6601-109">See also</span></span>

- [<span data-ttu-id="c6601-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6601-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

