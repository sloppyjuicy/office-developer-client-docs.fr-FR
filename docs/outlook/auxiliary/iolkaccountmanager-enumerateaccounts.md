---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtient un énumérateur pour les comptes de la catégorie spécifique ou un type.
ms.openlocfilehash: 091361ce2532bdffd3c78279861c0be4aa15d2ea
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788611"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Obtient un énumérateur pour les comptes de la catégorie spécifique ou un type.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Paramètres

_pclsidCategory_
  
> [in] L'identificateur de classe de la catégorie à énumérer. La valeur doit être une des opérations suivantes :
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [in] L'identificateur de classe du type de compte pour énumérer. La valeur doit être une des opérations suivantes :
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement. La seule valeur prise en charge est OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
   
## <a name="remarks"></a>Remarques

Spécification de valeur NULL pour la catégorie renvoie un énumérateur de tous les comptes du type spécifié. De même, la spécification NULL pour le type renvoie un énumérateur de tous les comptes de la catégorie spécifiée.
  
 **IOlkAccountManager::EnumerateAccounts** ne prend pas en charge la catégorie de carnet d'adresses pour un compte Exchange. Si le compte est un compte Exchange (*pclsidType* est **CLSID_OlkMAPIAccount ), et** que vous essayez d’éumer les comptes qui implémentent le carnet d’adresses (*prgclsidCategory* est **CLSID_OlkAddressBook** ), l’appel de **IOlkAccountManager::EnumerateAccounts** ne retournera pas le compte Exchange dans l’éumérateur de comptes *ppEnum* . 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

