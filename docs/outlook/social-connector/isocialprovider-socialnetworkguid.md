---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Renvoie un GUID qui représente un identificateur unique pour le réseaux sociaux.
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787617"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Renvoie un GUID qui représente un identificateur unique pour le réseaux sociaux.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Valeur de propriété

Pointeur vers une valeur GUID qui représente un identificateur unique pour le réseaux sociaux.
  
## <a name="remarks"></a>Remarques

Le GUID doit être immuable et ne doit pas changer même si la version du fournisseur change.
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

