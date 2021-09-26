---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialise le fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 4e41c78c016358c205f860345bee6cdcf3ba06e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608864"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialise le fournisseur Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Paramètres

_socialProviderInterfaceVersion_
  
> [in] Version des interfaces du fournisseur OSC attendues par l’OSC.
    
_languageTag_
  
> [in] Balise de langue IETF (Internet Engineering Task Force), définie par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)qui représente la langue d’interface utilisateur Outlook actuelle.
    
## <a name="remarks"></a>Remarques

Le format de version du  _paramètre socialProviderInterfaceVersion_ est  _X_. _xxxx_, où  _X_ est la version principale et  _xxxx_ la version mineure de l’OSC. Pour Office 2013, vérifiez que la version principale est 15. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

