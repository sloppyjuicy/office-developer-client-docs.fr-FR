---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message pour l’erreur spécifiée.
ms.openlocfilehash: 3a32c4bdb3bed1f98228670a5ac66f7d36f14855
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561893"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Obtient une chaîne de message pour l’erreur spécifiée. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Paramètres

_hr_
  
> [in] Code d’erreur à rechercher.
    
_ppwszError_
  
> [out] Le message d’erreur qui correspond à  *hr*  . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

