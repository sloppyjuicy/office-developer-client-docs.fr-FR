---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Enregistre un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.
ms.openlocfilehash: e17bd2b2f07761b8e381913a1de6113dd8133cad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625664"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Enregistre un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Paramètres

_pNotify_
  
> [in] Interface [IOlkAccountNotify](iolkaccountnotify.md) que le gestionnaire de comptes utilisera pour envoyer des notifications au client. 
    
_pdwCookie_
  
> [out] Un cookie que [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) utilisera lors de la suppression de l’inscription pour le compte. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un argument non valide a été fourni.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

