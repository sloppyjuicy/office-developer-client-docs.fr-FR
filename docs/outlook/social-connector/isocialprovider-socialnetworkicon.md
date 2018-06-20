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
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Renvoie un tableau d’octets qui représente l’icône du réseau social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Valeur de propriété

Pointeur vers une structure qui spécifie un tableau d’octets qui contient l’icône de réseau social.
  
## <a name="remarks"></a>Remarques

Les ressources image pris en charge sont les formats .png, .bmp et .jpeg.
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

