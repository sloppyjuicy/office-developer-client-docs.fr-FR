---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libère la mémoire allouée par l’interface IOlkAccountManager.
ms.openlocfilehash: e51aa8dd165e9cf1d1498386387b422404c7a5d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561928"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Libère la mémoire allouée par [l’interface IOlkAccountManager.](iolkaccountmanager.md) 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Paramètres

_pv_
  
> [in] Pointeur vers la mémoire à libérer.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Utilisez cette méthode pour libérer la mémoire allouée par [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Voir aussi

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

