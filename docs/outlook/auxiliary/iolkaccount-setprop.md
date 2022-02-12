---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Définit la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: 4a65f54fda2d0bc030b5fe4312e7ceded0eb8fd3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780203"
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
  
> [in] Balise de propriété de la propriété de compte à définir.
    
_pVar_
  
> [in] Valeur de la propriété spécifiée.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel de méthode a réussi. |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée. |
   
## <a name="remarks"></a>Remarques

Utilisez [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer les modifications apportées à la valeur des propriétés du compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

