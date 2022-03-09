---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message pour l’erreur spécifiée.
ms.openlocfilehash: 16e136f901d88a8d0d0186f52b0681b73a47bb7f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375698"
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
  
> [out] Message d’erreur correspondant à _hr_.

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs arguments ne sont pas valides. |

## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
