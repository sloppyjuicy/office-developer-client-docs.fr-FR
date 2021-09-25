---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtient le nom de profil d’un compte.
ms.openlocfilehash: d24f108aa4227ce8fe38e46b48a8f56a0eb29cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625685"
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
  
> [in] [out] Lors de l’appel de cette méthode, contient la taille (en nombre de  _caractères) de pwszIdentity_ qui a été allouée. Lors du retour, contient la longueur réelle, y compris le caractère de fin 0, du nom de profil renvoyé. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OUTOFMEMORY  <br/> |Le nom de profil renvoyé est plus long que la taille  _de pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ est NULL.  <br/> |
   
## <a name="remarks"></a>Remarques

Si  _pwszIdentity_ est trop petit pour contenir le nom du profil, il ne sera pas définie lors du retour et  _pcch_ pointera vers la taille requise pour  _pwszIdentity_.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

