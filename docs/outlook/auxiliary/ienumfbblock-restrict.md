---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Limite l'énumération à une période spécifiée.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317562"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Limite l'énumération à une période spécifiée.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Paramètres

_ftmStart_
  
>  dans L'heure de début pour limiter l'énumération. 
    
_ftmEnd_
  
> dans L'heure de fin pour restreindre l'énumération.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode réinitialise également l'énumération.
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

