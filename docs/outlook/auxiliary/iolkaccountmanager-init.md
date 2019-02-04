---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le Gestionnaire de comptes à utiliser.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: b361919ae2d3ac000d9fcaa3030713df7062ecd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2019
ms.locfileid: "29715339"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Initialise le Gestionnaire de comptes à utiliser.
  
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
  
> [in] Interface [IOlkAccountHelper](iolkaccounthelper.md) qui fournit des fonctionnalités d’assistance de compte. 
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement.
    
   - **ACCT_INIT_NO_STORES_CHECK** — empêche une synchronisation avec un magasin associé à un compte (par exemple, un compte IMAP). 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** — services MAPI empêche de la synchronisation avec des comptes. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** — empêche le Gestionnaire de comptes d’intercepter les messages de diffusion destinées aux autres applications. 
   
   - **OLK_ACCOUNT_NO_FLAGS** — services MAPI se synchronise avec les comptes. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** a déjà été appelée.  <br/> |
|E_OLK_REGISTRY  <br/> |Le Gestionnaire de comptes n’a pas pu accéder les paramètres de Registre nécessaires.  <br/> |
   
## <a name="remarks"></a>Remarques

Le client doit appeler **IOlkAccountManager::Init** pour initialiser le compte responsable avant d’utiliser le Gestionnaire de comptes pour accéder aux comptes ou configurer des notifications. Étant donné que Outlook synchronise automatiquement les services MAPI avec des comptes au démarrage, utilisez **ACCT_INIT_NOSYNCH_MAPI_ACCTS** sauf s’il existe une cause spécifique à synchroniser. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

