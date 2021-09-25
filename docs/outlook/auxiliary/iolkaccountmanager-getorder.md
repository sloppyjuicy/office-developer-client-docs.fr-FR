---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtient le classement de la catégorie de comptes spécifiée.
ms.openlocfilehash: 3a680e7a40197a3edf22e78d4e35ac981802a193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617110"
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
  
>  [out] Nombre de comptes. 
    
_prgAccts_
  
> [out] Pointeur vers un tableau de comptes.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, l’appelant alloue uniquement un pointeur de tableau  *prgAccts,*  mais pas de mémoire pour le tableau auquel  *prgAccts*  pointe. Après le retour de cette méthode, l’appelant doit utiliser [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) pour libérer la mémoire allouée pour  *prgAccts*  . 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

