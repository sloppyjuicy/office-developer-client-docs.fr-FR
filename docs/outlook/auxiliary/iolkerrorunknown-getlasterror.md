---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message pour l’erreur spécifiée.
ms.openlocfilehash: 3d510cb7141238e76ae1fa4ec6f26daf4c3abe62
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777599"
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
|S_OK  <br/> |L'appel a réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides. |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

