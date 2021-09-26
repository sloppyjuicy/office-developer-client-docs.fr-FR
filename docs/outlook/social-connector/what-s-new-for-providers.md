---
title: Nouveautés pour les fournisseurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Cette rubrique répertorie les principales modifications apportées Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1.1.
ms.openlocfilehash: a9f8836313ee49e0e3d7fa18ffcf1ee7e2babb75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598961"
---
# <a name="whats-new-for-providers"></a>Nouveautés pour les fournisseurs

Cette rubrique répertorie les principales modifications apportées Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1.1. Il décrit également les membres de l’interface et les éléments XML qui ont été ajoutés, modifiés ou supprimés. 
  
Dans Office 2013, OSC fonctionne avec non seulement Outlook, mais également SharePoint Server, SharePoint Workspace, le client Lync et toutes les autres applications clientes Office qui prendre en charge les informations de présence et la carte de visite. Un fournisseur OSC peut faire surface des mises à jour d’informations sociales dans **l’onglet NOUVEAUTÉS** du Outlook Contacts, ainsi que dans la carte de visite. 
  
Voici quelques modifications majeures apportées Outlook Social Connector 2013 : 
  
- Si un fournisseur prend en charge l’affichage des activités, il synchronise toujours les activités à la demande et ne s’appuie plus sur les activités précédemment mises en cache. Cela signifie que le fournisseur stocke les activités des amis et des non-amis en mémoire pour afficher des activités plus récentes.
    
- Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs sur Internet doivent utiliser le protocole HTTPS (Hypertext Transfer Protocol) avec SSL (Secure Socket Layer). Dans le cas contraire, il existe un risque que les adresses de messagerie, les activités de réseau social et d’autres données utilisateur sont interceptées ou exposées pendant le transit.
    
- Si vous avez des fournisseurs qui fonctionnent avec une version antérieure de Outlook, pour prendre en charge Office 2013, vous devez mettre à jour le package d’installation. Pour plus [d’informations, voir Liste](installation-checklist.md) de contrôle d’installation. 
    
Le tableau suivant indique la disponibilité de différentes fonctionnalités dans Outlook Social Connector 2013 par rapport à Outlook Social Connector 1.1.
  
|**Fonctionnalité**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interface utilisateur final  <br/> |SharePoint Serveur, espace SharePoint de travail, client Lync, carte de visite dans toutes les applications clientes Office et volet Contacts dans Outlook  <br/> |Volet Personnes dans Outlook  <br/> |
|Authentification de base  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification basée sur les formulaires  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification mise en cache  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation mise en cache pour le dossier d’amis avec les contacts dans la boutique par défaut  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation des activités mises en cache pour les amis avec le dossier **d’activités masqué**  <br/> |Non  <br/> |Oui  <br/> |
|Synchronisation à la demande (image, nom, titre) pour les amis et les non-amis sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation des activités à la demande pour les amis et les non-amis sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Suivre sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Ne pas suivre sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Visiter la page de profil utilisateur  <br/> |Via un lien  <br/> |Via un badge réseau  <br/> |
|Observation des paramètres de confidentialité sur le réseau social (par exemple, affichage du profil et des activités des non-amis qui autorisent l’affichage de tels éléments)  <br/> |Oui  <br/> |Oui  <br/> |
|Adresses e-mail hachées transmises au fournisseur  <br/> |Oui  <br/> |Oui  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Modifications par rapport à la version précédente de l’extensibilité du fournisseur OSC

Le tableau suivant indique les membres qui ont été ajoutés ou sont supprimés de l’interface correspondante.
  
|**Interface et membre**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Supprimé dans Outlook Social Connector 2013. Notez **que ISocialSession::GetActivities** a également été supprimé depuis Outlook Social Connector 1.1.  <br/> Pour synchroniser les flux d’activités, vous devez implémenter la méthode [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Définissez **dynamicActivitiesLookupEx** sur **true,** ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.  <br/> |
   
Le tableau suivant indique les éléments de schéma qui ont été modifiés.
  
|**Élément Schema**|**Comment**|
|:-----|:-----|
|**fonctionnalités** <br/> |Ajouté dans Outlook Social Connector 2013 : **élément allowChangesToAutoConfigure.**  <br/> Supprimé dans Outlook Social Connector 2013 : **élément cacheActivities.**  <br/> |
|**person** <br/> |Ajouté dans Outlook Social Connector 2013 : **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, industries , **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools**, and **website** elements.   <br/> |
   
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [XML pour les amis](xml-for-friends.md)
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

