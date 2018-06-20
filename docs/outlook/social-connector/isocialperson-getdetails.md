---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtient une chaîne qui représente les détails de la personne, telles que le prénom, nom et une URL vers une image de profil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787585"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtient une chaîne qui représente les détails de la personne, telles que le prénom, nom et une URL vers une image de profil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Paramètres

_plus d’informations_
  
> [out] Une valeur de chaîne XML qui représente les détails d’une personne.
    
## <a name="remarks"></a>Remarques

La chaîne XML renvoyée _Détails_ doit être conformes à la définition de schéma pour la **personne**, telle que définie dans le schéma pour l’extensibilité de fournisseur Outlook Social Connector (OSC).
  
L’OSC appelle **GetDetails** si la mise en cache de la prise en charge du fournisseur OSC ou synchronisation hybride d’amis sur le réseaux sociaux. Lorsque l’OSC obtient initialement activités amis pour l’utilisateur connecté, il appelle [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et stocke les informations de vos amis dans un dossier contacts spécifique au réseau social, dans le magasin d’Outlook par défaut de l’utilisateur ayant ouvert une session sur . Par la suite l’OSC n’appelle **GetFriendsAndColleagues** ou **GetDetails** , sauf si l’intervalle d’actualisation du cache a expiré. Pour plus d’informations sur la façon dont l’OSC met en cache les informations de vos amis dans un dossier contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

