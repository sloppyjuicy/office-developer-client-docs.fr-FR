---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Définit la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431987"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Définit la valeur de la propriété de compte spécifiée.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Paramètres

_dwProp_
  
> dans Balise de propriété de la propriété Account à définir.
    
_pVar_
  
> dans Valeur de la propriété spécifiée.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel de la méthode a réussi.  <br/> |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) pour enregistrer les modifications apportées à la valeur des propriétés du compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

