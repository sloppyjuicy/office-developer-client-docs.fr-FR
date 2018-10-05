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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385829"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialise le fournisseur Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Paramètres

_socialProviderInterfaceVersion_
  
> [in] La version des interfaces de fournisseur OSC attendue par le OSC.
    
_languageTag_
  
> [in] La balise de langue Internet Engineering Task Force (IETF), définie par la [[norme RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), qui représente la langue d’interface utilisateur Outlook active.
    
## <a name="remarks"></a>Remarques

Le format de version pour le paramètre _socialProviderInterfaceVersion_ est _X_. _xxxx_, où _X_ est la version principale et _xxxx_ est la version secondaire de la OSC. Pour Office 2013, recherchez la version principale est 15. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

