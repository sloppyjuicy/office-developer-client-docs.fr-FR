---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Désinsère un client auprès du gestionnaire de comptes pour les notifications pour tous les comptes.
ms.openlocfilehash: db49af76751e48b1daf011f9b46e4607e34d64c2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784355"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Désinsère un client auprès du gestionnaire de comptes pour les notifications pour tous les comptes. 
  
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
|S_OK  <br/> |L'appel a réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

