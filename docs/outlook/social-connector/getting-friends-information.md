---
title: Obtention des informations sur les amis
description: Décrit comment osc appelle des méthodes dans une séquence pour obtenir des informations et des images pour les amis sur le réseau social.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
ms.openlocfilehash: 3af7056c2c9aa17d5a3bac31a720c46fcc5704d5
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853901"
---
# <a name="getting-friends-information"></a>Obtention des informations sur les amis

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getFriends** et **cacheFriends** dans les **fonctionnalités retournées** XML indiquent que le fournisseur OSC prend en charge l’obtention d’amis et la mise en cache d’amis en tant qu’éléments de contact Outlook dans un dossier de contacts correspondant, l’OSC peut effectuer la séquence d’appel suivante. L’OSC appelle des méthodes dans cette séquence pour obtenir des informations et des images (prises en charge par l’interface [ISocialPerson](isocialpersoniunknown.md) ) pour les amis sur le réseau social. 
  
> [!NOTE]
> Le système d’exploitation actualise le cache à un intervalle par défaut. Si une erreur se produit lors de l’actualisation du cache, l’OSC effectue de nouvelles tentatives à un autre intervalle prédéfistré, qui peut également être contrôlé en spécifiant l’élément **contactSyncRestartInterval** dans le code XML **des fonctionnalités** . Pour plus d’informations sur l’actualisation du cache des contacts, consultez [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) : l’OSC obtient l’ID d’utilisateur de l’utilisateur Office connecté au réseau social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) : à l’aide de l’ID d’utilisateur de l’utilisateur Office, l’OSC obtient un objet **ISocialPerson** pour cet utilisateur. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) : l’OSC obtient la liste des amis de l’utilisateur sur le réseau social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) : pour chaque personne dans le code XML retourné par **GetFriendsAndColleagues**, l’OSC obtient une interface **ISocialPerson** . 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) : pour chaque personne dans le code XML retourné par **GetFriendsAndColleagues**, l’OSC obtient une ressource d’image.
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

