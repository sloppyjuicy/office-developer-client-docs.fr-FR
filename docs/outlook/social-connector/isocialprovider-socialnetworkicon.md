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
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787728"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="25975-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="25975-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="25975-104">Renvoie un tableau d’octets qui représente l’icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="25975-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="25975-105">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="25975-105">Property value</span></span>

<span data-ttu-id="25975-106">Pointeur vers une structure qui spécifie un tableau d’octets qui contient l’icône de réseau social.</span><span class="sxs-lookup"><span data-stu-id="25975-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25975-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="25975-107">Remarks</span></span>

<span data-ttu-id="25975-108">Les ressources image pris en charge sont les formats .png, .bmp et .jpeg.</span><span class="sxs-lookup"><span data-stu-id="25975-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25975-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25975-109">See also</span></span>

- [<span data-ttu-id="25975-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25975-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

