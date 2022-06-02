---
title: ISocialPersonGetFriendsAndColleagues
description: Décrit la syntaxe, les paramètres et les remarques pour ISocialPersonGetFriendsAndColleagues, qui obtient une chaîne qui représente une collection de personnes.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
ms.openlocfilehash: 6de4ec6a0de416e74114b5e4aee31d7d06b3f181
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853859"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtient une chaîne qui représente une collection de personnes.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsCollection_
  
> [out] Chaîne XML qui représente un ensemble d’amis de la personne et qui est conforme à la définition **d’amis** telle que définie dans le schéma XML pour Outlook l’extensibilité du fournisseur OSC (Social Connector). 
    
## <a name="remarks"></a>Remarques

L’OSC appelle **GetFriendsAndColleagues** si le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride d’amis sur le réseau social. Lorsque l’OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l’utilisateur Outlook connecté au réseau social, **GetFriendsAndColleagues** retourne une chaîne XML qui représente les amis de l’utilisateur connecté sur le réseau social. La chaîne XML est conforme à la définition de schéma XML **d’amis** et spécifie un élément **de personne** (qui est également conforme à la définition de schéma du fournisseur OSC) pour chaque ami. 
  
Lorsque **GetFriendsAndColleagues** retourne les informations d’amis pour l’utilisateur connecté, le système d’exploitation stocke ces informations dans un dossier de contacts. Ce dossier est spécifique au réseau social et se trouve dans le magasin de Outlook par défaut de l’utilisateur connecté. Pour plus d’informations sur la façon dont osc met en cache les informations des amis dans un dossier de contacts, consultez [Synchroniser les amis et les activités](synchronizing-friends-and-activities.md).
  
Les informations pour chaque ami retourné dans le paramètre _personsCollection_ sont conformes à la définition de schéma XML pour **la personne**. L’élément **person** prend en charge de nombreuses informations pour chaque ami, notamment les adresses e-mail SMTP (qui correspondent aux éléments **emailAddress**, **emailAddress2** et **emailAddress3** ) que l’ami a spécifiés sur le réseau social, et l’ID d’utilisateur (qui correspond à **l’élément userID** ) qui identifie cet ami sur le réseau social. 
  
Pour afficher les activités d’un utilisateur Outlook sélectionné dans le volet Contacts, le système d’exploitation tente de mettre en correspondance l’utilisateur avec chaque ami renvoyé par **GetFriendsAndColleagues**. Pour ce faire, le système d’exploitation met en correspondance l’adresse SMTP de l’utilisateur Outlook sélectionné avec les adresses e-mail que chaque ami a spécifiées sur le réseau social. Si l’OSC trouve une adresse e-mail SMTP correspondante, l’OSC utilise **l’ID utilisateur** correspondant de l’ami pour appeler la méthode [ISocialSession::GetPerson](isocialsession-getperson.md) . Il fait cela pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour cet ami, qui permet ensuite à la OSC d’obtenir des activités et des photos de cet ami à partir du réseau social. 
  
Toutefois, si l’utilisateur Outlook sélectionné ne spécifie pas cette même adresse SMTP sur un compte sur le réseau social, ou si l’utilisateur Outlook n’a pas de compte sur ce réseau social, le osc ne pourra pas trouver de correspondance pour cet utilisateur et n’affichera aucune activité pour cet utilisateur sur le réseau social.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtention d’informations sur les amis](getting-friends-information.md)

