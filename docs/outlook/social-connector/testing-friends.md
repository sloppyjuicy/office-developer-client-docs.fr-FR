---
title: Test des amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Cette rubrique décrit des tests et des scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) renvoie correctement les données d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433667"
---
# <a name="testing-friends"></a>Test des amis

Cette rubrique décrit des tests et des scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) renvoie correctement les données d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Synchronisation mise en cache

Un fournisseur OSC implémente [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), que l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation mise en cache des données des amis. Après avoir appelé [ISocialPerson::GetFriendsAndColleagues,](isocialperson-getfriendsandcolleagues.md)l’OSC stocke les données des amis renvoyés dans un dossier de contacts spécifique au réseau social dans le magasin d’Outlook par défaut de l’utilisateur connecté. L’OSC appelle également [ISocialSession::GetPerson](isocialsession-getperson.md) et [ISocialPerson::GetPicture](isocialperson-getpicture.md) pour obtenir une image de profil pour chaque ami. 
  
### <a name="initiate-synchronization"></a>Lancer la synchronisation

Pour lancer la synchronisation, vous pouvez activer et utiliser le bouton de débogage **Synchroniser** les contacts dans le composant ruban de l’interface utilisateur Microsoft Office Fluent. Pour plus d’informations sur les boutons de débogage OSC, voir [Débogage d’un fournisseur.](debugging-a-provider.md) 
  
### <a name="test-scenarios"></a>Scénarios de test

Testez les éléments suivants pour vérifier que les données des amis sont correctement mises en cache.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Dossier Contacts  <br/> |Le dossier de contacts propre au réseau social existe dans le magasin de contacts par défaut de l’Outlook utilisateur.  <br/> |
|Données des amis renvoyées par **ISocialPerson::GetFriendsAndColleagues** <br/> |Chaque ami correspond à un contact dans le dossier contacts propre au réseau.  <br/> |
|Données des amis  <br/> |Les champs de contact de chaque ami ont les données correctes.  <br/> |
|Images de profil des amis renvoyées par **ISocialPerson::GetPicture** <br/> |L’élément de contact de chaque ami contient l’image de profil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Un fournisseur OSC implémente **ISocialProvider::GetCapabilities**, que l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation à la demande des amis et des non-amis. Pour les personnes affichées dans le volet Personnes de Outlook, l’OSC obtient et hait ses adresses SMTP, appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)et stocke (en mémoire) les données renvoyées pour ces personnes. 
  
### <a name="determining-friends-and-non-friends"></a>Détermination des amis et des non-amis

Les adresses SMTP hachées transmises à **GetPeopleDetails** sont essentielles pour déterminer si une personne est un ami ou non. Si une personne n’inclut pas cette adresse SMTP dans son compte de réseau social, ou même si cette personne est un ami par une adresse e-mail différente sur le réseau social, **GetPeopleDetails** renvoie toujours **nonfriend** for that person as the **friendStatus** in the  _personsCollection_ parameter. En outre, pour une personne qui n’est pas un ami mais qui spécifie l’adresse SMTP dans son compte de réseau social, les données renvoyées incluent uniquement ce qui est disponible pour un non-ami comme autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test pour des amis et des non-amis

Pour créer un sujet de test pour un ami, identifiez l’adresse SMTP d’une personne qui inclut cette adresse dans son compte de réseau social et qui a un statut d’ami avec l’utilisateur connecté sur ce réseau. Créez un message électronique qui inclut cette adresse SMTP. De même, pour créer un sujet de test pour un non-ami, identifiez l’adresse SMTP d’une personne qui n’est pas un ami de l’utilisateur connecté par cette adresse, mais qui a spécifié dans ses paramètres de confidentialité pour permettre aux non-amis d’afficher leurs activités sur le réseau social. Créez un message électronique qui inclut cette adresse SMTP. 
  
Dans l Outlook’explorateur, lorsque vous sélectionnez le message électronique qui inclut un ami (ou un non-ami), le volet Personnes affiche les destinataires. La sélection de l’ami (ou non- ami) dans le volet Personnes vous permet de tester que le fournisseur fournit des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que votre fournisseur fournit correctement des informations sur les amis et les non-amis, testez les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|La personne sélectionnée dans le volet Personnes est un ami de l’utilisateur connecté sur le réseau social.  <br/> |Le volet Personnes affiche les activités de cette personne sur le réseau social.  <br/> |
|La personne sélectionnée dans le volet Personnes est un non-ami de l’utilisateur connecté sur le réseau social, mais a autorisé l’affichage de ses activités par des non-amis.  <br/> |Le volet Personnes affiche les activités de cette personne sur le réseau social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Synchronisation hybride

Si un fournisseur OSC prend en charge la synchronisation hybride d’amis et de non-amis, l’OSC fait les choses suivantes : 
  
- OsC stocke les informations des amis de l’utilisateur connecté dans le dossier de contacts spécifique au réseau social.
    
- L’OSC récupère les informations pour les non-amis à la demande à partir du réseau social et les stocke uniquement en mémoire, mais pas dans un dossier.
    
Pour tester la synchronisation hybride, suivez les suggestions de test dans la section Synchronisation mise en [cache](#olosc_TestingFriends_CachedSync) pour les amis et celles de la [section](#olosc_TestingFriends_OnDemandSync) Synchronisation à la demande pour les non-amis. 
  
## <a name="see-also"></a>Voir aussi

- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md) 
- [XML pour les amis](xml-for-friends.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

