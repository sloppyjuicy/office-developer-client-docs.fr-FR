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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787598"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_résultat_
  
> [out] Chaîne XML qui représente les fonctionnalités d’un fournisseur Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Remarques

La chaîne XML renvoyée _résultat_ doit être conformes à la définition de schéma pour l’élément de **fonctionnalités** , comme défini dans le schéma XML d’extensibilité du fournisseur OSC. 
  
Le fournisseur doit renvoyer une chaîne de _résultat_ pour activer les appels suivants à partir de l’OSC au fournisseur fonctionner correctement. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

