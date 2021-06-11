---
title: Obtention des informations sur les amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Le Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428794"
---
# <a name="getting-friends-information"></a>Obtention des informations sur les amis

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getFriends** et **cacheFriends** dans les fonctionnalités **renvoyées** XML indiquent que le fournisseur OSC prend en charge l’obtention d’amis et la mise en cache d’amis en tant qu’éléments de contact Outlook dans un dossier de contacts correspondant, l’OSC peut effectuer la séquence d’appels suivante. L’OSC appelle les méthodes de cette séquence pour obtenir des informations et des images (telles que prises en charge par l’interface [ISocialPerson)](isocialpersoniunknown.md) pour les amis sur le réseau social. 
  
> [!NOTE]
> OsC actualise le cache à un intervalle par défaut. Si une erreur se produit lors de l’actualisation du cache, l’OSC réessaie à un autre intervalle prédéfinis, qui peut également être contrôlé en spécifiant l’élément **contactSyncRestartInterval** dans le **XML** des fonctionnalités. Pour plus d’informations sur l’actualisation du cache de contacts, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) : OSC obtient l’ID de l’utilisateur Office connecté au réseau social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) : à l’aide de l’ID d’utilisateur de l’utilisateur Office, OSC obtient un **objet ISocialPerson** pour cet utilisateur. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) : OSC obtient la liste des amis de l’utilisateur sur le réseau social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — Pour chaque personne dans le XML renvoyé par **GetFriendsAndColleagues**, l’OSC obtient une interface **ISocialPerson.** 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — Pour chaque personne dans le XML renvoyé par **GetFriendsAndColleagues**, l’OSC obtient une ressource d’image.
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

