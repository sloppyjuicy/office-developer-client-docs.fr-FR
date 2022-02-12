---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Supprime le compte spécifié.
ms.openlocfilehash: 250180bf076f7c90d7fd66c419cc2751430fe5ba
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778936"
---
# <a name="iolkaccountmanagerdeleteaccount"></a>IOlkAccountManager::DeleteAccount

Supprime le compte spécifié.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a>Paramètres

_dwAcctID_
  
> [in] ID de compte du compte à supprimer.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Le compte spécifié est in trouver. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)

