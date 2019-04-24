---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtient une valeur de type String qui représente les détails de la personne, tels que le prénom, le nom et l'URL d'une image de profil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286142"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtient une valeur de type String qui représente les détails de la personne, tels que le prénom, le nom et l'URL d'une image de profil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Paramètres

_détails_
  
> remarquer Valeur de chaîne XML qui représente les détails d'une personne.
    
## <a name="remarks"></a>Remarques

La chaîne XML de _Détails_ renvoyée doit être conforme à la définition de schéma pour **Person**, comme défini dans le schéma pour l'extensibilité du fournisseur Outlook Social Connector (OSC).
  
L'OSC appelle **GetDetails** si le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride des amis sur le réseau social. Lorsque l'objet OSC Obtient initialement des activités de Friends pour l'utilisateur connecté, il appelle [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et stocke les informations des amis dans un dossier de contacts spécifique au réseau social, dans la Banque Outlook par défaut de l'utilisateur connecté. . Par la suite, OSC n'appelle pas **GetFriendsAndColleagues** ou **GetDetails** , sauf si l'intervalle d'actualisation du cache a expiré. Pour plus d'informations sur la façon dont OSC met en cache les informations des amis dans un dossier contacts, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

