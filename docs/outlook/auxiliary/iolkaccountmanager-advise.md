---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Inscrit un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322196"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Inscrit un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.
  
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
  
> dans Interface [IOlkAccountNotify](iolkaccountnotify.md) qui sera utilisée par le gestionnaire de comptes pour envoyer des notifications au client. 
    
_pdwCookie_
  
> remarquer Un cookie que [IOlkAccountManager::](iolkaccountmanager-unadvise.md) Unadvise utilisera lors de la suppression de l'inscription pour le compte. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un argument non valide a été fourni.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

