---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtient la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: 2ab86eeaf18374a28159c6f0743e55d1664a1b31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561949"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtient la valeur de la propriété de compte spécifiée.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Paramètres

_dwProp_
  
> [in] Balise de propriété de la propriété de compte à obtenir.
    
_pVar_
  
> [out] Valeur de la propriété spécifiée.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |La propriété n’est pas trouvée pour le compte donné.  <br/> |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Après le retour de cette méthode, si la valeur de la propriété de compte est binaire ou de type chaîne, vous devez libérer  *pVar*  à l’aide de [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

