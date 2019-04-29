---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Recherche un compte par valeur de propriété.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428801"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Recherche un compte par valeur de propriété.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Paramètres

_dwProp_
  
> dans Propriété sur laquelle porte la recherche. Doit être [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> dans Valeur à respecter.
    
_ppAccount_
  
> remarquer Le compte trouvé. Cet objet prend en charge une interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Le compte spécifié est introuvable.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [ACCT_VARIANT](acct_variant.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

