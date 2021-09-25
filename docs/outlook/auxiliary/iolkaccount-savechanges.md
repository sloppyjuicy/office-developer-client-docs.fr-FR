---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre.
ms.openlocfilehash: 2ea5cfaa51ae4fada6d771b8aac774bf309a0335
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561935"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Paramètres

_dwFlags_
  
> [in] Indicateurs pour modifier le comportement. OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La méthode a réussi.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Impossible de trouver le compte spécifié.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="remarks"></a>Remarques

Après avoir changé la valeur des propriétés du compte à l’aide [d’IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccount::SaveChanges** pour enregistrer ces modifications. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

