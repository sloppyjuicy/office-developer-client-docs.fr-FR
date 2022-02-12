---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Recherche un compte par valeur de propriété.
ms.openlocfilehash: 18fa6aa08b3c819440d47825174b7082b3a413f2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784348"
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
  
> [in] Propriété sur qui effectuer la recherche. Doit être [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> [in] Valeur à mettre en correspondance.
    
_ppAccount_
  
> [out] Compte trouvé. Cet objet prend en charge une interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_ACCT_NOT_FOUND  <br/> |Le compte spécifié est in trouver. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
   
## <a name="see-also"></a>Voir aussi

- [ACCT_VARIANT](acct_variant.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

