---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtient une valeur de type String qui décrit les fonctionnalités du fournisseur.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408102"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtient une valeur de type String qui décrit les fonctionnalités du fournisseur.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_result_
  
> remarquer Chaîne XML qui représente les fonctionnalités d'un fournisseur Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Remarques

La chaîne XML de _résultats_ renvoyée doit être conforme à la définition de schéma pour l'élément **Capabilities** , comme défini dans le schéma XML pour l'extensibilité du fournisseur OSC. 
  
Le fournisseur doit retourner une chaîne de _résultats_ pour permettre aux appels suivants du OSC au fournisseur de fonctionner correctement. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

