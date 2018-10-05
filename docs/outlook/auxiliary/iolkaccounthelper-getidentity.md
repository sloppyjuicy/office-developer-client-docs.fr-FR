---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtient le nom du profil d’un compte.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400137"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Obtient le nom du profil d’un compte.
  
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
  
> [in] [out] Lors de l’appel de cette méthode contient la taille (en nombre de caractères) de _pwszIdentity_ qui a été affectée. Au retour, contient la longueur réelle, y compris le caractère de fin de 0, le nom de profil retourné. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OUTOFMEMORY  <br/> |Le nom du profil retourné est supérieure à la taille de _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ est NULL.  <br/> |
   
## <a name="remarks"></a>Remarques

Si _pwszIdentity_ est trop petit pour contenir le nom du profil, ne sera pas être défini sur retour et pointe vers la taille requise pour _pwszIdentity_ _pcch_ .
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

