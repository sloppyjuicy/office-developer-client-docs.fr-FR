---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Désinsère un client auprès du gestionnaire de comptes pour les notifications de tous les comptes.
ms.openlocfilehash: cc82aa8bc3ba7f550f1f328c12a68802ef34c29c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631236"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Désinsère un client auprès du gestionnaire de comptes pour les notifications de tous les comptes. 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>Paramètres

_dwCookie_
  
> [in] Cookie renvoyé par [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

