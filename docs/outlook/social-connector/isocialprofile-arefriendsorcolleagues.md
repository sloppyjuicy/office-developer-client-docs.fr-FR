---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Détermine si les utilisateurs spécifiés sont amis.
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787591"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Détermine si les utilisateurs spécifiés sont amis.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Paramètres

_ID utilisateur_
  
> [in] Structure qui spécifie un tableau de valeurs d’ID utilisateur qui correspondent à un ensemble de personnes sur le réseau social.
    
_résultats_
  
> [out] Pointeur vers une structure qui spécifie un tableau de valeurs Boolean qui indique si la personne correspondante dans le tableau des _ID utilisateur_ est un ami. 
    
## <a name="remarks"></a>Remarques

Pour chaque personne représentée dans le tableau d’entrée du paramètre _userIds_ , cette méthode définit l’élément correspondant dans le tableau de sortie du paramètre _résultats_ . **true** indique que la personne est un ami, et **false** indique que la personne n’est pas un ami. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

