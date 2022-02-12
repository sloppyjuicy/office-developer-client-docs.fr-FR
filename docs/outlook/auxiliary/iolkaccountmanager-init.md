---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le gestionnaire de comptes à utiliser.
ms.openlocfilehash: b9d50176298636104779ed5d5a170b1d109642da
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781575"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Initialise le gestionnaire de comptes à utiliser.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Paramètres

_pAcctHelper_
  
> [in] Interface [IOlkAccountHelper](iolkaccounthelper.md) qui fournit la fonctionnalité d’aide de compte. 
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement.
    
   - **ACCT_INIT_NO_STORES_CHECK** : empêche un compte (tel qu’un compte IMAP) de se synchroniser avec une banque associée. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** : empêche les services MAPI de se synchroniser avec les comptes. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** : empêche le gestionnaire de comptes d’intercepter les messages de diffusion destinés à d’autres applications. 
   
   - **OLK_ACCOUNT_NO_FLAGS** — Synchronise les services MAPI avec les comptes. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** a déjà été appelé. |
|E_OLK_REGISTRY  <br/> |Le gestionnaire de comptes n’a pas pu accéder aux paramètres de Registre requis. |
   
## <a name="remarks"></a>Remarques

Le client doit appeler **IOlkAccountManager::Init** pour initialiser le gestionnaire de comptes avant d’utiliser le gestionnaire de comptes pour accéder aux comptes ou configurer des notifications. Étant donné Outlook synchronise automatiquement les services MAPI avec les comptes au démarrage, utilisez ACCT_INIT_NOSYNCH_MAPI_ACCTS sauf s’il existe une cause spécifique à synchroniser. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

