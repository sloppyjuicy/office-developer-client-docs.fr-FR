---
title: Obtention des informations sur les amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Outlook Social Connector (OSC) appelle la méthode ISocialProvider:: GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286321"
---
# <a name="getting-friends-information"></a>Obtention des informations sur les amis

Outlook Social Connector (OSC) appelle la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getFriends** et **cacheFriends** dans le code XML des **fonctionnalités** renvoyées indiquent que le fournisseur OSC prend en charge l'obtention des amis et la mise en cache des amis en tant qu'éléments de contact Outlook dans un dossier de contacts correspondant, le OSC peut créer séquence d'appel suivante. Le OSC appelle des méthodes dans cette séquence pour obtenir des informations et des images (telles que prises en charge par l'interface [ISocialPerson](isocialpersoniunknown.md) ) pour les amis sur le réseau social. 
  
> [!NOTE]
> Le OSC actualise le cache à un intervalle par défaut. Si une erreur se produit lors de l'actualisation du cache, OSC effectue une nouvelle tentative à un autre intervalle prédéfini, qui peut également être contrôlé en spécifiant l'élément **contactSyncRestartInterval** dans le code XML des **fonctionnalités** . Pour plus d'informations sur l'actualisation du cache de contacts, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession:: LoggedOnUserID](isocialsession-loggedonuserid.md) : le OSC Obtient l'ID d'utilisateur de l'utilisateur Office qui est connecté au réseau social. 
    
2. [ISocialSession:: GetPerson](isocialsession-getperson.md) : à l'aide de l'ID d'utilisateur de l'utilisateur Office, le OSC Obtient un objet **ISocialPerson** pour cet utilisateur. 
    
3. [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — le OSC Obtient la liste des amis de l'utilisateur sur le réseau social. 
    
4. [ISocialSession:: GetPerson](isocialsession-getperson.md) : pour chaque personne figurant dans le code XML renvoyé par **GetFriendsAndColleagues**, l'interface OSC Obtient une interface **ISocialPerson** . 
    
5. [ISocialPerson:: GetPicture,](isocialperson-getpicture.md) : pour chaque personne figurant dans le code XML renvoyé par **GetFriendsAndColleagues**, OSC Obtient une ressource image.
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

