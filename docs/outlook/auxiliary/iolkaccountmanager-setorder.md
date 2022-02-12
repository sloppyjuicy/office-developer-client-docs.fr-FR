---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifie l’ordre de la catégorie de comptes spécifiée.
ms.openlocfilehash: 3e809852aec64e2fcec6b4cac470c67a044cca41
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788604"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Modifie l’ordre de la catégorie de comptes spécifiée.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Paramètres

_pclsidCategory_
  
> [in] ID de classe de catégorie pour lequel définir la commande. La valeur doit être l’une des suivantes :
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] Nombre de comptes.
    
_rgAccts_
  
> [in] Tableau d’ID de compte. La taille du tableau est  _cAccts_.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Le nouvel ordre de tri a un nombre de comptes différent de l’ancien. |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
   
## <a name="remarks"></a>Remarques

L’appelant alloue de la mémoire pour le pointeur de tableau  _prgAccts_ ainsi que pour le tableau auquel  _prgAccts_ pointe. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

