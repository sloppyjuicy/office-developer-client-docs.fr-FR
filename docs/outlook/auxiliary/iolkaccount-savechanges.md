---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valide les modifications de l’objet account en écrivant dans le magasin de Registre.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782660"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Valide les modifications de l’objet account en écrivant dans le magasin de Registre.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Paramètres

_dwFlags_
  
> [in] Indicateurs pour modifier le comportement. OLK_ACCOUNT_NO_FLAGS est la seule valeur pris en charge.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La méthode a réussi.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Impossible de trouver le compte spécifié.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
   
## <a name="remarks"></a>Remarques

Après avoir modifié la valeur des propriétés de compte à l’aide de [IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccount::SaveChanges** pour enregistrer ces modifications. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

