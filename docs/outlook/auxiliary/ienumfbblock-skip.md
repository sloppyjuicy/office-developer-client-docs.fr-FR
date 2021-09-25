---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Ignore un nombre spécifié de blocs de données de libre/occupé.
ms.openlocfilehash: baf13acb36d1455873771f1191461b7d17677959
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580411"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

Ignore un nombre spécifié de blocs de données de libre/occupé.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a>Paramètres

_celt_
  
>  [in] Nombre de blocs de libre/occupé à ignorer. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)

