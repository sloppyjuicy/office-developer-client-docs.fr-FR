---
title: Obtention d’informations sur vos amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: L’Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787575"
---
# <a name="getting-friends-information"></a>Obtention d’informations sur vos amis

L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getFriends** et **cacheFriends** dans le renvoyée XML des **capacités** indiquent que le fournisseur OSC prend en charge la mise en route d’amis et éléments dans un dossier contacts correspondant de contact amis mise en cache comme Outlook, l’OSC peut-il la séquence d’appel suivante. L’OSC appelle des méthodes dans l’ordre ci-après pour obtenir des informations et des images (comme pris en charge par l’interface [ISocialPerson](isocialpersoniunknown.md) ) pour vos amis sur le réseaux sociaux. 
  
> [!NOTE]
> L’OSC actualise le cache selon un intervalle par défaut. Si une erreur se produit au cours du cache Actualiser, les tentatives OSC à un autre intervalle prédéfini, qui peut également être contrôlé en spécifiant l’élément **contactSyncRestartInterval** dans le XML des **fonctionnalités** . Pour plus d’informations sur l’actualisation du cache de contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — le OSC Obtient l’ID d’utilisateur de l’utilisateur d’Office qui est connecté au réseau social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) — avec l’ID d’utilisateur de l’utilisateur d’Office, l’OSC Obtient un objet **ISocialPerson** pour cet utilisateur. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — l’OSC Obtient la liste ami de l’utilisateur sur le réseau social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — pour chaque personne dans le code XML renvoyé par **GetFriendsAndColleagues**, l’OSC Obtient une interface **ISocialPerson** . 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — pour chaque personne dans le code XML renvoyé par **GetFriendsAndColleagues**, l’OSC Obtient une ressource de l’image.
    
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

