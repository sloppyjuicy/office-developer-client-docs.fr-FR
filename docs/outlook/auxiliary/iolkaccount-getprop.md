---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtient la valeur de la propriété du compte spécifié.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782662"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtient la valeur de la propriété du compte spécifié.
  
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
  
> [in] La balise de propriété de la propriété de compte à obtenir.
    
_pVar_
  
> [out] La valeur de la propriété spécifiée.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |La propriété est introuvable pour le compte donné.  <br/> |
|E_INVALIDARG  <br/> |Une balise de propriété non valide a été spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Une fois que cette méthode est retournée, si la valeur de la propriété de compte est un type de fichier binaire ou chaîne, vous devez libérer *pVar* à l’aide de [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

