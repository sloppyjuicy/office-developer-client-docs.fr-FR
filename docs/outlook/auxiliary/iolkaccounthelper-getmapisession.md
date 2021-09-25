---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Ouvre une session MAPI et maintient une référence à la session pour le gestionnaire de comptes.
ms.openlocfilehash: 460317b5b83c3d2ef6aca26260d797502f7ea084
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617124"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Ouvre une session MAPI et maintient une référence à la session pour le gestionnaire de comptes.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Paramètres

_ppmsess_
  
> [out] Session MAPI en cours.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

En raison de problèmes de référence circulaire, le gestionnaire de comptes lui-même ne peut pas conserver la référence pour la session MAPI.
  
## <a name="see-also"></a>Voir aussi

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession : IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

