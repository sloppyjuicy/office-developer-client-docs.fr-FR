---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Enregistre les modifications apportées au compte spécifié.
ms.openlocfilehash: 26c5d29a38aafd17c4e76aa025327f89ca53a970
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776633"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Enregistre les modifications apportées au compte spécifié.
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Paramètres

_dwAcctID_
  
> [in] ID de compte à enregistrer. 
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement. OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Le compte spécifié est in trouver. |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation. |
   
## <a name="remarks"></a>Remarques

Après avoir changé la valeur des propriétés du compte à l’aide [d’IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccountManager::SaveChanges** ou [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer ces modifications. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

