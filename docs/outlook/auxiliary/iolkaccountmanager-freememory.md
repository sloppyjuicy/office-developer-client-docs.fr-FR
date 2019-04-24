---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libère la mémoire allouée par l'interface IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322056"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Libère la mémoire allouée par l'interface [IOlkAccountManager](iolkaccountmanager.md) . 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Paramètres

_PV_
  
> dans Pointeur vers la mémoire à libérer.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Utilisez cette méthode pour libérer de la mémoire allouée par [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Voir aussi

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

