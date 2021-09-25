---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
ms.openlocfilehash: d0c6772d38d0bdf6d1c6d3b482eb0dc7b70f7f50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574509"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_result_
  
> [out] Chaîne XML qui représente les fonctionnalités d’un fournisseur Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Remarques

La  _chaîne_ XML de résultat renvoyée doit être conforme à la définition de schéma de l’élément **capabilities,** tel que défini dans le schéma XML pour l’extensibilité du fournisseur OSC. 
  
Le fournisseur doit renvoyer une chaîne  _de_ résultats pour permettre aux appels ultérieurs de l’OSC au fournisseur de fonctionner correctement. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

