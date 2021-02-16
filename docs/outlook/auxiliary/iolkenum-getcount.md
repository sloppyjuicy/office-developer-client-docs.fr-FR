---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtient le nombre de comptes dans l’éumérateur.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421822"
---
# <a name="iolkenumgetcount"></a>IOlkEnum::GetCount

Obtient le nombre de comptes dans l’éumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a>Paramètres

_qu’est-ce que c'_
  
> [out] Pointeur vers le nombre d’objets en cours d’éumation.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

