---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Limite l’éumération à une période spécifiée.
ms.openlocfilehash: 0dcb2cb2304323a4d434bb315531190f36e96e96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596609"
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
  
>  [in] Heure de début pour limiter l’éumération. 
    
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

