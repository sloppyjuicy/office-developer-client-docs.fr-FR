---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425833"
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

