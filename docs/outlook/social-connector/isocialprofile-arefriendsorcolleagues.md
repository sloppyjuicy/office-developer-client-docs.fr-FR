---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Détermine si les utilisateurs spécifiés sont des amis.
ms.openlocfilehash: 5f782e998f46485cc5560e13ffbe55394702dbc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563216"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Détermine si les utilisateurs spécifiés sont des amis.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Paramètres

_userIds_
  
> [in] Structure qui spécifie un tableau de valeurs d’ID d’utilisateur qui correspondent à un ensemble de personnes sur le réseau social.
    
_results_
  
> [out] Pointeur vers une structure qui spécifie un tableau de valeurs Boolean, indiquant si la personne correspondante dans le tableau  _userIds_ est un ami. 
    
## <a name="remarks"></a>Remarques

Pour chaque personne représentée dans le tableau d’entrée du paramètre  _userIds,_ cette méthode définit l’élément correspondant dans le tableau de sortie du  _paramètre de_ résultats. **true** indique que la personne est un ami, et **false** indique que la personne n’est pas un ami. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

