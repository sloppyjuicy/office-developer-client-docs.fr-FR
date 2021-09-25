---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignore un nombre spécifié de comptes dans l’éumérateur.
ms.openlocfilehash: c8c7dbcf58b5e66de4291a489f8afd3a71474eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617089"
---
# <a name="iolkenumskip"></a>IOlkEnum::Skip

Ignore un nombre spécifié de comptes dans l’éumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a>Paramètres

_cSkip_
  
> [in] Nombre de comptes à ignorer.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [IOlkEnum::GetCount](iolkenum-getcount.md) 
- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)

