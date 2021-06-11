---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Renvoie un tableau d’octets qui représente l’icône du réseau social.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438686"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="1f12a-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="1f12a-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="1f12a-104">Renvoie un tableau d’octets qui représente l’icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="1f12a-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="1f12a-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1f12a-105">Property value</span></span>

<span data-ttu-id="1f12a-106">Pointeur vers une structure qui spécifie un tableau d’octets qui contient l’icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="1f12a-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f12a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f12a-107">Remarks</span></span>

<span data-ttu-id="1f12a-108">Les ressources d’image .bmp, .jpeg et les formats .png pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1f12a-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f12a-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f12a-109">See also</span></span>

- [<span data-ttu-id="1f12a-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f12a-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

