---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787623"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsAddresses_
  
> [in] Chaîne XML qui spécifie les adresses SMTP de hachage d’un ensemble d’utilisateurs.
    
_personsCollection_
  
> [out] Chaîne XML qui contient une collection de détails de la personne et de l’image.
    
## <a name="remarks"></a>Remarques

L’Outlook Social Connector (OSC) appelle **GetPeopleDetails** si le fournisseur OSC prend en charge la synchronisation à la demande ou hybride de vos amis et non amis. 
  
Le paramètre _personsAddresses_ doit être conforme à la définition de schéma pour **hashedAddresses**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC. La chaîne _personsAddresses_ représente un ensemble de hachage adresses SMTP pour chaque utilisateur affiché dans le volet personnes. L’utilisateur ne dispose pas à un ami de l’utilisateur connecté, représenté par la propriété [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . Les adresses SMTP hachage sont chiffrés à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans du fournisseur **fonctionnalités** XML. L’OSC identifie chaque **hashedAddress** dans la collection _personAddresses_ avec un élément **d’index** . Le fournisseur doit utiliser l’élément **d’index** pour identifier le destinataire **personne** XML lorsqu’elle retourne **amis** XML pour **GetPeopleDetails**. Si le destinataire n’est pas un utilisateur inscrit sur le réseaux sociaux, le fournisseur ne doit pas retourner toute **personne** XML du destinataire. L’élément **d’index** pour chaque utilisateur réseau représenté par une **personne** XML correspond à l’élément **d’index** pour le destinataire dans _personsAddresses_.
  
L’OSC stocke les informations renvoyées par le paramètre _personsCollection_ en mémoire. La chaîne XML _personsCollection_ doit être conforme à la définition de schéma pour des **amis**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC. Pour plus d’informations sur la façon dont l’OSC utilise et met à jour ces informations en mémoire, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)

