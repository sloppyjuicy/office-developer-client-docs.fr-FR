---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Annule l'inscription d'un client avec le gestionnaire de comptes pour les notifications pour tous les comptes.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322007"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Annule l'inscription d'un client avec le gestionnaire de comptes pour les notifications pour tous les comptes. 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>Paramètres

_dwCookie_
  
> dans Cookie renvoyé par [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md).
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

