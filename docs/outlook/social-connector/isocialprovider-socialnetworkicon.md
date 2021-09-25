---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Renvoie un tableau d’octets qui représente l’icône du réseau social.
ms.openlocfilehash: f5c2b2744364f159545d72e8a2525562acc90d06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594922"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Renvoie un tableau d’octets qui représente l’icône du réseau social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une structure qui spécifie un tableau d’octets qui contient l’icône du réseau social.
  
## <a name="remarks"></a>Remarques

Les ressources d’image .bmp, .jpeg et les formats .png pris en charge.
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

