---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408102"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_result_
  
> [out] Chaîne XML qui représente les fonctionnalités d’un fournisseur Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Remarques

La  _chaîne_ XML de résultat renvoyée doit être conforme à la définition de schéma de l’élément **capabilities,** tel que défini dans le schéma XML pour l’extensibilité du fournisseur OSC. 
  
Le fournisseur doit renvoyer une chaîne  _de_ résultats pour permettre aux appels ultérieurs de l’OSC au fournisseur de fonctionner correctement. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

