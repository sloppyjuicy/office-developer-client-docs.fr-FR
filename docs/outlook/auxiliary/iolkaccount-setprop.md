---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Définit la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: 8fd8eb0acc51d457911799e751451e7600202d5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617145"
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
|S_OK  <br/> |L’appel de méthode a réussi.  <br/> |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer les modifications apportées à la valeur des propriétés du compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

