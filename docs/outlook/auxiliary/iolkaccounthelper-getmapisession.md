---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392599"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Paramètres

_ppmsess_
  
> [out] La session MAPI en cours.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

En raison de problèmes de référence circulaire, le Gestionnaire de comptes lui-même ne peut pas mettre à jour la référence de la session MAPI.
  
## <a name="see-also"></a>Voir aussi

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession : IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

