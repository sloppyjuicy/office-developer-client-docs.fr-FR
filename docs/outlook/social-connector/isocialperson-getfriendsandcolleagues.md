---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtient une chaîne qui représente une collection de personnes.
ms.openlocfilehash: 09526b32d1dbba5d285b4e5917fcc60a2f583fe0
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462557"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtient une chaîne qui représente une collection de personnes.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsCollection_
  
> [out] Chaîne XML qui représente un ensemble d’amis de la personne et qui est conforme à la définition des amis telle  que définie dans le schéma XML pour l’extensibilité du fournisseur Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Remarques

L’OSC appelle **GetFriendsAndColleagues** si le fournisseur OSC prend en charge la synchronisation hybride ou mise en cache des amis sur le réseau social. Lorsque l’OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l’utilisateur Outlook connecté au réseau social, **GetFriendsAndColleagues** renvoie une chaîne XML qui représente les amis de l’utilisateur connecté sur le réseau social. La chaîne XML est conforme à la définition de **schéma XML** des amis et spécifie un  élément person (qui est également conforme à la définition de schéma du fournisseur OSC) pour chaque ami. 
  
Lorsque **GetFriendsAndColleagues** renvoie les informations d’amis de l’utilisateur connecté, l’OSC les stocke dans un dossier de contacts. Ce dossier est spécifique au réseau social et réside dans le magasin d’informations par défaut de l’utilisateur Outlook connecté. Pour plus d’informations sur la façon dont OSC met en cache les informations des amis dans un dossier de contacts, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
Les informations de chaque ami renvoyé dans le _paramètre personsCollection_ sont conformes à la définition de schéma XML de la **personne**. L’élément person prend en charge de nombreux éléments d’informations pour chaque ami, y compris les adresses de messagerie SMTP (qui m’indiquent les éléments **emailAddress**, **emailAddress2** et **emailAddress3**) que l’ami a spécifiés sur le réseau social et l’ID d’utilisateur (qui est mapillé avec l’élément **userID**) qui identifie cet ami sur le réseau social. 
  
Pour afficher les activités d’un utilisateur Outlook sélectionné dans le volet Personnes, l’OSC tente de faire correspondre l’utilisateur à chaque ami renvoyé par **GetFriendsAndColleagues**. Pour ce faire, l’OSC fait correspondre l’adresse SMTP de l’utilisateur Outlook sélectionné avec les adresses de messagerie que chaque ami a spécifiées sur le réseau social. Si l’OSC trouve une adresse de messagerie SMTP correspondante, l’OSC utilise **l’ID** d’utilisateur correspondant de l’ami pour appeler la méthode [ISocialSession::GetPerson](isocialsession-getperson.md) . Il le fait pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour cet ami, qui permet ensuite à l’OSC d’obtenir des activités et des images de cet ami à partir du réseau social. 
  
Toutefois, si l’utilisateur Outlook sélectionné ne spécifie pas cette même adresse SMTP sur un compte sur le réseau social, ou si l’utilisateur Outlook n’a pas de compte sur ce réseau social, l’OSC ne pourra pas trouver de correspondance pour cet utilisateur et n’affichera aucune activité pour cet utilisateur sur le réseau social.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtention d’informations sur les amis](getting-friends-information.md)

