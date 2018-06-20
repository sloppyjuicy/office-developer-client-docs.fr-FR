---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Définit la valeur de la propriété du compte spécifié.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782679"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Définit la valeur de la propriété du compte spécifié.
  
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
  
> [in] La balise de propriété de la propriété de compte à définir.
    
_pVar_
  
> [in] La valeur de la propriété spécifiée.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel de méthode a réussi.  <br/> |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer les modifications apportées à la valeur des propriétés de compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

