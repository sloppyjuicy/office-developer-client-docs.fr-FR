---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtient une chaîne qui représente une collection de personnes.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787594"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtient une chaîne qui représente une collection de personnes.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Paramètres

_personsCollection_
  
> [out] Chaîne XML qui représente un ensemble d’amis ou de la personne, et qui est conforme à la définition de **vos amis** définis dans le schéma XML pour l’extensibilité de fournisseur Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Remarques

L’OSC appelle **GetFriendsAndColleagues** si la mise en cache de la prise en charge du fournisseur OSC ou synchronisation hybride d’amis sur le réseaux sociaux. Lorsque l’OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l’utilisateur Outlook qui est connecté au réseau social, **GetFriendsAndColleagues** renvoie une chaîne XML qui représente des amis de l’utilisateur connecté sur le réseau social. La chaîne XML conforme à la définition de schéma XML **amis** et spécifie un élément de la **personne** (qui également conforme à la définition de schéma de fournisseur OSC) pour chacun d'entre eux. 
  
Lorsque **GetFriendsAndColleagues** renvoie des informations pour l’utilisateur connecté amis, l’OSC stocke ces informations dans un dossier contacts. Ce dossier est spécifique au réseau social et réside dans le magasin d’Outlook ouvert une session sur l’utilisateur par défaut. Pour plus d’informations sur la façon dont l’OSC met en cache les informations de vos amis dans un dossier contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
Informations pour chaque ami retournée dans le paramètre _personsCollection_ est conforme à la définition de schéma XML pour la **personne**. L’élément **personne** prend en charge plusieurs éléments d’information pour chaque ami, y compris les adresses de messagerie SMTP (qui correspondent aux éléments **emailAddress**, **emailAddress2**et **emailAddress3** ) que votre ami a spécifié sur la réseau social et l’ID utilisateur (qui correspond à l’élément **userID** ) qui identifie ce friend sur le réseaux sociaux. 
  
Pour afficher les activités pour un utilisateur Outlook sélectionné dans le volet personnes, l’OSC tente de faire correspondre l’utilisateur avec chaque ami renvoyé à partir de **GetFriendsAndColleagues**. Pour cela, la OSC correspondant à l’adresse SMTP de l’utilisateur Outlook sélectionné avec les adresses de messagerie chaque ami a spécifié sur le réseau social. Si l’OSC détecte une adresse de messagerie SMTP correspondante, l’OSC utilise correspondant **userID** de votre ami pour appeler la méthode [ISocialSession::GetPerson](isocialsession-getperson.md) . Pour cela, pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour que friend, qui permet l’OSC obtenir les activités et les images de cet expéditeur à partir du réseau social. 
  
Toutefois, si l’utilisateur Outlook sélectionné ne spécifie pas cette même adresse SMTP sur un compte sur le réseaux sociaux, ou si l’utilisateur Outlook n’a pas de compte sur ce réseau social, l’OSC ne sera pas en mesure de trouver une correspondance pour cet utilisateur et n’affiche pas les activiti es pour cet utilisateur sur le réseau social.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtention d’informations sur des amis](getting-friends-information.md)

