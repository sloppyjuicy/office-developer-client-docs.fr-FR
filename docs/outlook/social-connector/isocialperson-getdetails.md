---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtient une chaîne qui représente les détails de la personne, tels que le prénom, le nom et l’URL d’une image de profil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427331"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtient une chaîne qui représente les détails de la personne, tels que le prénom, le nom et l’URL d’une image de profil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameters

_détails_
  
> [out] Valeur de chaîne XML qui représente les détails d’une personne.
    
## <a name="remarks"></a>Remarques

La chaîne XML de _détails_ renvoyée doit être conforme à la définition de schéma de la **personne,** telle que définie dans le schéma pour l’extensibilité du fournisseur Outlook Social Connector (OSC).
  
L’OSC appelle **GetDetails si** le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride des amis sur le réseau social. Lorsque l’OSC obtient initialement les activités des amis de l’utilisateur connecté, il appelle [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et stocke les informations des amis dans un dossier de contacts spécifique au réseau social, dans le magasin Outlook par défaut de l’utilisateur connecté. Par la suite, OSC n’appelle **pas GetFriendsAndColleagues** ou **GetDetails,** sauf si l’intervalle d’actualisation du cache a expiré. Pour plus d’informations sur la façon dont OSC met en cache les informations des amis dans un dossier de contacts, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

