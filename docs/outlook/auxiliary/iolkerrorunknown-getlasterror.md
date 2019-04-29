---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message pour l'erreur spécifiée.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431700"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Obtient une chaîne de message pour l'erreur spécifiée. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Paramètres

_confidentiel_
  
> dans Code d'erreur à rechercher.
    
_ppwszError_
  
> remarquer Message d'erreur correspondant à *RH* . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

