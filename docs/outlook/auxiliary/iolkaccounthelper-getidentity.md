---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtient le nom de profil d’un compte.
ms.openlocfilehash: d9e26e979ed1117cfb05f4ba5907bc61459c9b8b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370517"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Obtient le nom de profil d’un compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Paramètres

_pwszIdentity_
  
> [in] [out] Nom du profil.

_pcch_
  
> [in] [out] Lors de l’appel de cette méthode, contient la taille (en nombre de _caractères) de pwszIdentity_ qui a été allouée. Lors du retour, contient la longueur réelle, y compris le caractère de fin 0, du nom de profil renvoyé.

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|E_OUTOFMEMORY  <br/> |Le nom de profil renvoyé est plus long que la taille _de pwszIdentity_. |
|E_INVALIDARG  <br/> | _pcch_ est NULL. |

## <a name="remarks"></a>Remarques

Si _pwszIdentity_ est trop petit pour contenir le nom du profil, il ne sera pas définie lors de l’retour et _pcch_ pointera vers la taille requise pour _pwszIdentity_.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)
