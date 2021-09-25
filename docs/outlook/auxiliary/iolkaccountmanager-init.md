---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le gestionnaire de comptes à utiliser.
ms.openlocfilehash: 44742fadb2c0c450611370d700ced33173387a02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552002"
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
    
   - **ACCT_INIT_NO_STORES_CHECK** : empêche un compte (tel qu’un compte IMAP) de se synchroniser avec un magasin associé. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** : empêche les services MAPI de se synchroniser avec les comptes. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** : empêche le gestionnaire de comptes d’intercepter les messages de diffusion destinés à d’autres applications. 
   
   - **OLK_ACCOUNT_NO_FLAGS** : synchronise les services MAPI avec les comptes. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** a déjà été appelé.  <br/> |
|E_OLK_REGISTRY  <br/> |Le gestionnaire de comptes n’a pas pu accéder aux paramètres de Registre requis.  <br/> |
   
## <a name="remarks"></a>Remarques

Le client doit appeler **IOlkAccountManager::Init** pour initialiser le gestionnaire de comptes avant d’utiliser le gestionnaire de comptes pour accéder aux comptes ou configurer des notifications. Comme Outlook synchronise automatiquement les services MAPI avec les comptes au démarrage, utilisez **ACCT_INIT_NOSYNCH_MAPI_ACCTS** à moins qu’il n’existe une cause spécifique à synchroniser. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

