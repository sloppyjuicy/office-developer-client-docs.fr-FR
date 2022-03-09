---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtient le classement de la catégorie de comptes spécifiée.
ms.openlocfilehash: 9caa68407b6fb5682fffb53ccfbab13bc0aa91dd
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380556"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Obtient le classement de la catégorie de comptes spécifiée.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Paramètres

_pclsidCategory_
  
> [in] ID de classe de catégorie pour lequel obtenir la commande. La valeur doit être une des opérations suivantes :

   - CLSID_OlkMail

   - CLSID_OlkAddressBook

   - CLSID_OlkStore

_pcAccts_
  
> [out] Nombre de comptes.

_prgAccts_
  
> [out] Pointeur vers un tableau de comptes.

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, l’appelant alloue uniquement un pointeur de tableau *prgAccts* , mais pas de mémoire pour le tableau auquel *prgAccts* pointe. Après le retour de cette méthode, l’appelant doit utiliser [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) pour libérer la mémoire allouée pour *prgAccts*.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)
