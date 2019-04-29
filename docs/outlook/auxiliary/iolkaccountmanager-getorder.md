---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtient l'ordre de tri de la catégorie de comptes spécifiée.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424622"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Obtient l'ordre de tri de la catégorie de comptes spécifiée.
  
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
  
> dans ID de classe de catégorie pour lequel obtenir la commande. La valeur doit être une des opérations suivantes :
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  remarquer Nombre de comptes. 
    
_prgAccts_
  
> remarquer Pointeur vers un tableau de comptes.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="remarks"></a>Remarques

Avant d'appeler cette méthode, l'appelant alloue uniquement un pointeur de tableau *prgAccts* mais pas de mémoire pour le tableau auquel *prgAccts* pointe. Une fois cette méthode renvoyée, l'appelant doit utiliser [IOlkAccountManager:: FreeMemory](iolkaccountmanager-freememory.md) pour libérer la mémoire allouée pour *prgAccts* . 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

