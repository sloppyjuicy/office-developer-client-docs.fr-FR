---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Limite l’éumération à une période spécifiée.
ms.openlocfilehash: 20fafe28e8c19f4e67b19ec7aa2a0fe3cf6b6ed5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381662"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Limite l’éumération à une période spécifiée.
  
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
  
> [in] Heure de début pour limiter l’éumération. 
    
_ftmEnd_
  
> [in] Heure de fin pour limiter l’éumération.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode réinitialise également l’éumération.
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

