---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtient une valeur de type String qui représente une collection de personnes.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331660"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtient une valeur de type String qui représente une collection de personnes.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsCollection_
  
> remarquer Une chaîne XML qui représente un ensemble d'amis de la personne et qui est conforme à la définition des **amis** définie dans le schéma XML pour l'extensibilité du fournisseur OSC (Outlook Social Connector). 
    
## <a name="remarks"></a>Remarques

L'OSC appelle **GetFriendsAndColleagues** si le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride des amis sur le réseau social. Lorsque la méthode OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l'utilisateur Outlook qui est connecté au réseau social, **GetFriendsAndColleagues** renvoie une chaîne XML qui représente les amis de l'utilisateur connecté sur le réseau social. La chaîne XML est conforme à la **** définition de schéma XML friends et spécifie un élément **Person** (qui est également conforme à la définition de schéma du fournisseur OSC) pour chaque Friend. 
  
Lorsque **GetFriendsAndColleagues** renvoie les informations sur les amis de l'utilisateur connecté, OSC stocke ces informations dans un dossier de contacts. Ce dossier est propre au réseau social et réside dans la Banque Outlook par défaut de l'utilisateur connecté. Pour plus d'informations sur la façon dont OSC met en cache les informations des amis dans un dossier contacts, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
Les informations de chaque ami renvoyé dans le paramètre _personsCollection_ sont conformes à la définition de schéma XML pour **Person**. L'élément **Person** prend en charge de nombreux éléments d'information pour chaque ami, y compris les adresses de messagerie SMTP (qui correspondent aux éléments **EmailAddress**, **EmailAddress2**et **EmailAddress3** ) spécifiés par l'ami sur le réseau social et ID d'utilisateur (qui correspond à l'élément **userid** ) qui identifie cet ami sur le réseau social. 
  
Pour afficher les activités d'un utilisateur Outlook sélectionné dans le volet de personnes, le OSC tente de faire correspondre l'utilisateur avec chaque ami renvoyé depuis **GetFriendsAndColleagues**. Le OSC effectue cette opération en comparant l'adresse SMTP de l'utilisateur Outlook sélectionné aux adresses de messagerie spécifiées par chaque ami sur le réseau social. Si OSC trouve une adresse de messagerie SMTP correspondante, le OSC utilise l'ID de l' **utilisateur** correspondant pour appeler la méthode [ISocialSession:: GetPerson](isocialsession-getperson.md) . Il effectue cette opération pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour cet ami, qui lui permet d'obtenir des activités et des images de cet ami à partir du réseau social. 
  
Toutefois, si l'utilisateur Outlook sélectionné ne spécifie pas la même adresse SMTP sur un compte sur le réseau social ou si l'utilisateur Outlook ne dispose pas d'un compte sur ce réseau social, le OSC ne peut pas trouver de correspondance pour cet utilisateur et n'affiche aucune opération. es pour cet utilisateur sur le réseau social.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtention d'informations sur les amis](getting-friends-information.md)

