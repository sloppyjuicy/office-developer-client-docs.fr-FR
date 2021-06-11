---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Renvoie un GUID qui représente un identificateur unique pour le réseau social.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407871"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="1de31-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="1de31-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="1de31-104">Renvoie un GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="1de31-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="1de31-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1de31-105">Property value</span></span>

<span data-ttu-id="1de31-106">Pointeur vers une valeur GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="1de31-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1de31-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1de31-107">Remarks</span></span>

<span data-ttu-id="1de31-108">Le GUID doit être immuable et ne doit pas changer même si la version du fournisseur change.</span><span class="sxs-lookup"><span data-stu-id="1de31-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1de31-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1de31-109">See also</span></span>

- [<span data-ttu-id="1de31-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1de31-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

