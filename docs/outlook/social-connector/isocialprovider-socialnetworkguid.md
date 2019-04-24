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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285511"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="ffe60-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="ffe60-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="ffe60-104">Renvoie un GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ffe60-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="ffe60-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ffe60-105">Property value</span></span>

<span data-ttu-id="ffe60-106">Pointeur vers une valeur GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ffe60-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffe60-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffe60-107">Remarks</span></span>

<span data-ttu-id="ffe60-108">Le GUID doit être immuable et ne doit pas être modifié même si la version du fournisseur change.</span><span class="sxs-lookup"><span data-stu-id="ffe60-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ffe60-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffe60-109">See also</span></span>

- [<span data-ttu-id="ffe60-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ffe60-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

