---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialise le fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285758"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialise le fournisseur Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Paramètres

_socialProviderInterfaceVersion_
  
> dans La version des interfaces de fournisseur OSC attendues par OSC.
    
_languageTag_
  
> dans Balise de langue IETF (Internet Engineering Task Force), définie par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), qui représente la langue actuelle de l'interface utilisateur Outlook.
    
## <a name="remarks"></a>Remarques

Le format de version du paramètre _socialProviderInterfaceVersion_ est _X_. _xxxx_, où _X_ est la version principale et _xxxx_ la version mineure du OSC. Pour Office 2013, vérifiez que la version majeure est 15. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

