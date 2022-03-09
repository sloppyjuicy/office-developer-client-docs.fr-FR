---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Avertit le client des modifications apportées au compte spécifié.
ms.openlocfilehash: fba334e72aeb38bed91386ac10deec818b2036ae
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373276"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Avertit le client des modifications apportées au compte spécifié.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Paramètres

_dwNotify_
  
> [in] Type de notification. La valeur doit être l’une des suivantes :
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in] ID de compte du compte qui a été créé, modifié, supprimé ou pré-supprimé.
    
 _dwFlags_
  
> [in] Non utilisé. OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

