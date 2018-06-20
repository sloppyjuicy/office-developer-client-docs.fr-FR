---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Recherche un compte à la valeur de la propriété.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782715"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Recherche un compte à la valeur de la propriété.
  
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
  
> [in] La propriété à rechercher. Doit être [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> [in] La valeur de correspondance.
    
_ppAccount_
  
> [out] Le compte est trouvé. Cet objet prend en charge une interface [IOlkAccount](iolkaccount.md) . 
    
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

