---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344869"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsAddresses_
  
> dans Chaîne XML qui spécifie les adresses SMTP hachées d'un ensemble d'utilisateurs.
    
_personsCollection_
  
> remarquer Chaîne XML qui contient une collection de détails de personne et d'image.
    
## <a name="remarks"></a>Remarques

Outlook Social Connector (OSC) appelle **GetPeopleDetails** si le fournisseur OSC prend en charge la synchronisation à la demande ou hybride des amis et des non-amis. 
  
Le paramètre _personsAddresses_ doit être conforme à la définition de schéma pour **hashedAddresses**, comme défini dans le schéma de l'extensibilité du fournisseur OSC. La chaîne _personsAddresses_ représente un ensemble d'adresses SMTP hachées pour chaque utilisateur affiché dans le volet de personnes. L'utilisateur ne doit pas nécessairement être un ami de l'utilisateur connecté représenté par la propriété [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) . Les adresses SMTP hachées sont chiffrées à l'aide de la fonction de hachage spécifiée par l'élément **hashFunction** dans le code XML des **fonctionnalités** du fournisseur. L'élément OSC identifie chaque **hashedAddress** dans la collection _personAddresses_ à l'aide d'un élément **index** . Le fournisseur doit utiliser l'élément **index** pour identifier le code XML de la **personne** du destinataire lorsqu'il renvoie des **amis** XML pour **GetPeopleDetails**. Si le destinataire n'est pas un utilisateur inscrit sur le réseau social, le fournisseur ne doit pas **** renvoyer de code XML pour ce destinataire. L'élément **index** de chaque utilisateur réseau représenté par la **personne** XML correspond à l'élément **index** du destinataire dans _personsAddresses_.
  
L'OSC stocke les informations renvoyées par le paramètre _personsCollection_ en mémoire. La chaîne XML _personsCollection_ doit être conforme à la définition de schéma pour les **amis**, comme défini dans le schéma pour l'extensibilité du fournisseur OSC. Pour plus d'informations sur l'utilisation et la mise à jour de ces informations en mémoire par le OSC, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)

