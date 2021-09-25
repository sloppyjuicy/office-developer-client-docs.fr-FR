---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libère la mémoire allouée par l’interface IOlkAccount.
ms.openlocfilehash: 5c8c0952c3014e3088e30565fdfed377d943f126
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576556"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Libère la mémoire allouée par l’interface [IOlkAccount.](iolkaccount.md) 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Paramètres

_pv_
  
> [in] Pointeur vers la mémoire à libérer.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Utilisez cette méthode pour libérer de la mémoire allouée par [IOlkAccount::GetProp](iolkaccount-getprop.md) (si la valeur de la propriété de compte spécifiée est un type binaire ou de chaîne) et [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Voir aussi

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

