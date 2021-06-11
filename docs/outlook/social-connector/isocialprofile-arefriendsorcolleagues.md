---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Détermine si les utilisateurs spécifiés sont des amis.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412561"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Détermine si les utilisateurs spécifiés sont des amis.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameters

_userIds_
  
> [in] Structure qui spécifie un tableau de valeurs d’ID d’utilisateur qui correspondent à un ensemble de personnes sur le réseau social.
    
_results_
  
> [out] Pointeur vers une structure qui spécifie un tableau de valeurs Boolean, indiquant si la personne correspondante dans le tableau  _userIds_ est un ami. 
    
## <a name="remarks"></a>Remarques

Pour chaque personne représentée dans le tableau d’entrée du paramètre  _userIds,_ cette méthode définit l’élément correspondant dans le tableau de sortie du  _paramètre de_ résultats. **true** indique que la personne est un ami, et **false** indique que la personne n’est pas un ami. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

