---
title: Test des amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Cette rubrique décrit les tests et les scénarios permettant de vérifier que le fournisseur Outlook Social Connector (OSC) retourne correctement les données des amis et des non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338786"
---
# <a name="testing-friends"></a>Test des amis

Cette rubrique décrit les tests et les scénarios permettant de vérifier que le fournisseur Outlook Social Connector (OSC) retourne correctement les données des amis et des non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Synchronisation mise en cache

Un fournisseur OSC implémente [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md), que l'OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation mise en cache des données des amis. Après l'appel de [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), OSC stocke les données des amis renvoyées dans un dossier de contacts spécifique au réseau social dans la Banque Outlook par défaut de l'utilisateur connecté. Le OSC appelle également [ISocialSession:: GetPerson](isocialsession-getperson.md) et [ISocialPerson:: GetPicture,](isocialperson-getpicture.md) pour obtenir une image de profil pour chaque ami. 
  
### <a name="initiate-synchronization"></a>Lancer la synchronisation

Pour lancer la synchronisation, vous pouvez activer et utiliser le bouton déboguer synchroniser les **contacts** dans le composant de ruban de l'interface utilisateur Microsoft Office Fluent. Pour plus d'informations sur les boutons de débogage OSC, consultez [la rubrique débogage d'un fournisseur](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Scénarios de test

Testez les éléments suivants pour vérifier que les données des amis sont correctement mises en cache.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Dossier de contacts  <br/> |Le dossier de contacts spécifique au réseau social existe dans la Banque Outlook par défaut de l'utilisateur.  <br/> |
|Données des amis renvoyées par **ISocialPerson:: GetFriendsAndColleagues** <br/> |Chaque ami correspond à un contact dans le dossier contacts spécifique au réseau.  <br/> |
|Données des amis  <br/> |Les champs de contact de chaque ami possèdent les données correctes.  <br/> |
|Images de profil des amis renvoyées par **ISocialPerson:: GetPicture,** <br/> |L'élément de contact de chaque ami contient l'image de profil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Un fournisseur OSC implémente **ISocialProvider:: GetCapabilities**, que l'OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation à la demande des amis et des non-Friends. Pour les personnes affichées dans le volet Outlook, le OSC Obtient et hache leurs adresses SMTP, appelle [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)et stocke (en mémoire) les données renvoyées pour ces personnes. 
  
### <a name="determining-friends-and-non-friends"></a>Détermination des amis et des non-amis

Les adresses SMTP hachées transmises à **GetPeopleDetails** sont les clés permettant de déterminer si une personne est un ami ou non un ami. Si une personne n'inclut pas cette adresse SMTP dans son compte de réseau social, ou même si elle est un ami par une adresse de messagerie différente sur le réseau social, **GetPeopleDetails** continue de renvoyer non **Friend** de cette personne en tant **que friendStatus** dans le paramètre _personsCollection_ . Par ailleurs, pour une personne qui n'est pas un ami mais qui spécifie l'adresse SMTP dans son compte de réseau social, les données renvoyées incluent uniquement ce qui est disponible pour un non-Friend, comme autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test pour des amis et des non-amis

Pour créer un objet de test pour un ami, identifiez l'adresse SMTP d'une personne qui inclut cette adresse dans son compte de réseau social et qui a un État Friend avec l'utilisateur connecté sur ce réseau. Créez un message électronique qui inclut cette adresse SMTP. De même, pour créer un objet de test pour un non-ami, identifiez l'adresse SMTP d'une personne qui n'est pas un ami de l'utilisateur connecté par cette adresse, et qui a déjà spécifié dans ses paramètres de confidentialité pour autoriser les personnes non friendes à consulter leurs activités sur le réseau social. k. Créez un message électronique qui inclut cette adresse SMTP. 
  
Dans l'explorateur Outlook, lorsque vous sélectionnez le message électronique qui comprend un ami (ou non un ami), le volet contacts affiche les destinataires. La sélection de l'option Friend (ou non-Friend) dans le volet contacts vous permet de vérifier que le fournisseur fournit des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que votre fournisseur fournit des informations sur les amis et les non-amis de manière appropriée, testez les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Personne sélectionnée dans le volet de personnes est un ami avec l'utilisateur connecté sur le réseau social.  <br/> |Le volet de contacts affiche les activités de cette personne sur le réseau social.  <br/> |
|Personne sélectionnée dans le volet de personnes est un non-ami de l'utilisateur connecté sur le réseau social, mais a autorisé ses activités à être visualisées par des non-Friends.  <br/> |Le volet de contacts affiche les activités de cette personne sur le réseau social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Synchronisation hybride

Si un fournisseur OSC prend en charge la synchronisation hybride des amis et des non-amis, le OSC effectue les opérations suivantes: 
  
- OSC stocke des informations pour les amis de l'utilisateur connecté dans le dossier de contacts spécifique au réseau social.
    
- Le OSC récupère des informations pour les non-amis à la demande à partir du réseau social et les stocke uniquement en mémoire, mais pas dans un dossier.
    
Pour tester la synchronisation hybride, suivez les suggestions de test de la section [synchronisation mise en cache](#olosc_TestingFriends_CachedSync) pour les amis et celles figurant dans la section [synchronisation à la demande](#olosc_TestingFriends_OnDemandSync) pour les non-amis. 
  
## <a name="see-also"></a>Voir aussi

- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md) 
- [XML pour les amis](xml-for-friends.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

