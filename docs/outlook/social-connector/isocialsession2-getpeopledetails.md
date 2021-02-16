---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Renvoie une chaîne qui contient une collection de détails de personne et d’image pour les utilisateurs spécifiés par le paramètre personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404532"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Renvoie une chaîne qui contient une collection de détails de personne et d’image pour les utilisateurs spécifiés par le paramètre _personsAddresses._ 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsAddresses_
  
> [in] Chaîne XML qui spécifie les adresses SMTP hachées d’un ensemble d’utilisateurs.
    
_personsCollection_
  
> [out] Chaîne XML qui contient une collection de détails de personne et d’image.
    
## <a name="remarks"></a>Remarques

Outlook Social Connector (OSC) appelle **GetPeopleDetails** si le fournisseur OSC prend en charge la synchronisation à la demande ou hybride des amis et non-amis. 
  
Le  _paramètre personsAddresses_ doit être conforme à la définition de schéma pour **hashedAddresses**, telle que définie dans le schéma pour l’extensibilité du fournisseur OSC. La  _chaîne personsAddresses_ représente un ensemble d’adresses SMTP hachées pour chaque utilisateur affiché dans le volet Personnes. L’utilisateur n’a pas besoin d’être un ami de l’utilisateur connecté représenté par la propriété [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) Les adresses SMTP hachées sont chiffrées à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans le code XML des fonctionnalités **du** fournisseur. L’OSC identifie chaque **hachageAddress** dans la collection _personAddresses_ avec un **élément index.** Le fournisseur doit utiliser **l’élément d’index** pour identifier le **XML** de la personne du destinataire lorsqu’il renvoie des amis **XML** pour **GetPeopleDetails**. Si le destinataire n’est pas un utilisateur inscrit sur le réseau social, le fournisseur ne doit retourner aucun **XML** de personne pour ce destinataire. **L’élément d’index** pour chaque utilisateur réseau représenté par une personne **XML** correspond à **l’élément d’index** pour le destinataire _dans personsAddresses_.
  
L’OSC stocke les informations renvoyées par le  _paramètre personsCollection_ en mémoire. La  _chaîne XML personsCollection_ doit être conforme à la définition de schéma pour les **amis,** telle que définie dans le schéma pour l’extensibilité du fournisseur OSC. Pour plus d’informations sur la façon dont OSC utilise et met à jour ces informations en mémoire, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)

