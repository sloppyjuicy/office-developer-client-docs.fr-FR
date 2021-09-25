---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Renvoie une chaîne qui représente le nom du réseau social.
ms.openlocfilehash: 400765e72567bb5e24bf806c279a02619ccefaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574516"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Renvoie une chaîne qui représente le nom du réseau social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le nom du réseau social.
  
## <a name="remarks"></a>Remarques

Outlook Les fournisseurs OSC (Social Connector) doivent localiser le nom du réseau social.
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

