---
title: Test des amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Cette rubrique décrit les tests et scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) renvoie correctement les données des amis et non-amis, le cas échéant, selon le mode de synchronisation pris en charge par le fournisseur.
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787727"
---
# <a name="testing-friends"></a>Test des amis

Cette rubrique décrit les tests et scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) renvoie correctement les données des amis et non-amis, le cas échéant, selon le mode de synchronisation pris en charge par le fournisseur.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Synchronisation mis en cache

Un fournisseur OSC implémente [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), qui l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation de mise en cache de données de vos amis. Après avoir appelé [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), l’OSC stocke les données d’amis renvoyée dans un dossier contacts spécifique au réseau social dans le magasin d’Outlook ouvert une session sur l’utilisateur par défaut. L’OSC appelle également [ISocialSession::GetPerson](isocialsession-getperson.md) et [ISocialPerson::GetPicture](isocialperson-getpicture.md) pour obtenir une image de profil pour chacun d'entre eux. 
  
### <a name="initiate-synchronization"></a>Lancer une synchronisation

Pour lancer une synchronisation, vous pouvez activer et utiliser le bouton de débogage **Synchroniser les Contacts** dans le composant du ruban de l’interface utilisateur Microsoft Office Fluent. Pour plus d’informations sur les boutons de débogage OSC, consultez [débogage d’un fournisseur](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Scénarios de test

Tester les éléments suivants pour vérifier que les données de vos amis sont correctement mis en cache.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Dossier contacts  <br/> |Le dossier des contacts spécifiques du réseau social existe dans le magasin d’Outlook par défaut de l’utilisateur.  <br/> |
|Données amis renvoyées par **ISocialPerson::GetFriendsAndColleagues** <br/> |Chacun d'entre eux correspond à un contact dans le dossier contacts spécifiques du réseau.  <br/> |
|Données amis  <br/> |Champs de contact pour chacun d'entre eux ont les données correctes.  <br/> |
|Images de profil amis renvoyés par **ISocialPerson::GetPicture** <br/> |L’élément de contact pour chaque ami contient l’image de profil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation de la demande

Un fournisseur OSC implémente **ISocialProvider::GetCapabilities**, qui l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation de la demande de vos amis et non amis. Pour les personnes affichées dans le volet personnes Outlook, obtient l’OSC et hachages leur SMTP résout, appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)et stocke (en mémoire) les données retournées pour ces personnes. 
  
### <a name="determining-friends-and-non-friends"></a>Détermination des amis et non amis

Les adresses SMTP hachage passés à **GetPeopleDetails** sont les clés pour déterminer si une personne est un ami ou un autre ami. Si une personne n’inclut pas d’adresse SMTP dans son compte de réseau social, ou même si cette personne est un ami par une autre adresse e-mail sur le réseaux sociaux, **GetPeopleDetails** renvoie toujours **nonfriend** correspondant à cette personne en tant que la ** friendStatus** dans le paramètre _personsCollection_ . Également, pour une personne qui n’est pas un ami, mais spécifie l’adresse SMTP dans son compte de réseaux sociaux, les données renvoyées incluent uniquement ce qui est disponible à un non-ami autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test d’amis ou non amis

Pour créer un objet de test pour un ami, identifier l’adresse SMTP d’une personne qui inclut cette adresse dans son compte de réseau social et qui a le statut ami avec l’utilisateur connecté à ce réseau. Créer un message électronique qui contient l’adresse SMTP. De même, pour créer un objet de test pour un ami-non, identifier l’adresse SMTP d’une personne qui n’est pas un ami de l’utilisateur connecté à cette adresse, et qui a encore spécifié dans ses paramètres de confidentialité pour autoriser non amis afficher leurs activités sur le réseau social. k. Créer un message électronique qui contient l’adresse SMTP. 
  
Dans l’Explorateur Outlook, lorsque vous sélectionnez le message électronique qui inclut un ami (ou non ami), le volet personnes affiche les destinataires. Sélection l’ami (ou non ami) dans le volet personnes permet à tester que le fournisseur est fournissant des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que votre fournisseur est fournissant des informations sur vos amis et non amis tester de manière appropriée, pour les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Personne sélectionnée dans le volet personnes est un ami avec l’utilisateur connecté sur le réseau social.  <br/> |Le volet personnes affiche les activités de la personne sur le réseau social.  <br/> |
|Personne sélectionnée dans le volet personnes n’est un ami de l’utilisateur connecté sur le réseau social, mais a permis à ses activités par non amis.  <br/> |Le volet personnes affiche les activités de la personne sur le réseau social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Synchronisation hybride

Si un fournisseur OSC prend en charge la synchronisation hybride des amis et non amis, l’OSC effectue les opérations suivantes : 
  
- L’OSC stocke des informations pour vos amis de l’utilisateur connecté dans le dossier contact spécifiques du réseau social.
    
- L’OSC récupère des informations non amis sur demande à partir du réseau social et le stocke en mémoire uniquement, mais pas dans un dossier.
    
Pour tester la synchronisation hybride, suivez les suggestions de tests dans la section [Mise en cache de la synchronisation](#olosc_TestingFriends_CachedSync) de vos amis, ainsi que ceux de la section [Synchronisation de la demande](#olosc_TestingFriends_OnDemandSync) non amis. 
  
## <a name="see-also"></a>Voir aussi

- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md) 
- [Code XML des amis](xml-for-friends.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

