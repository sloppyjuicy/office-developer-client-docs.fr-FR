---
title: Nouveautés pour les fournisseurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Cette rubrique répertorie les principales modifications apportées à Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1,1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329112"
---
# <a name="whats-new-for-providers"></a>Nouveautés pour les fournisseurs

Cette rubrique répertorie les principales modifications apportées à Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1,1. Il décrit également les membres d'interface et les éléments XML qui ont été ajoutés, modifiés ou déconseillés. 
  
Dans Office 2013, le OSC fonctionne avec non seulement Outlook, mais également SharePoint Server, SharePoint Workspace, le client Lync et toutes les autres applications clientes Office qui prennent en charge les informations de présence et la carte de visite. Un fournisseur OSC peut mettre en surface des mises à jour d'informations sociales sous l'onglet **WHAT'S New** du volet contacts Outlook, ainsi que dans la carte de visite. 
  
Voici quelques-unes des principales modifications apportées à Outlook Social Connector 2013: 
  
- Si un fournisseur prend en charge l'affichage des activités, le fournisseur synchronise toujours les activités à la demande et ne s'appuie plus sur les activités précédemment mises en cache. Cela signifie que le fournisseur stocke des activités d'amis et de non-amis en mémoire pour afficher des activités plus récentes.
    
- Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs via Internet doivent utiliser le protocole HTTPs (Hypertext Transfer Protocol (HTTP) avec SSL (Secure Socket Layer)). Dans le cas contraire, il existe un risque que les adresses de messagerie, les activités du réseau social et d'autres données utilisateur soient interceptées ou exposées lors du transit.
    
- Si vous avez des fournisseurs qui fonctionnent avec une version antérieure d'Outlook, pour prendre en charge Office 2013, vous devez mettre à jour le package d'installation. Pour plus d'informations, consultez la rubrique [Installation Checklist](installation-checklist.md) . 
    
Le tableau suivant indique la disponibilité de différentes fonctionnalités dans Outlook Social Connector 2013 par rapport à Outlook Social Connector 1,1.
  
|**Fonctionnalité**|**Outlook Social Connector 2013**|**Outlook Social Connector 1,1**|
|:-----|:-----|:-----|
|Interface utilisateur final  <br/> |SharePoint Server, SharePoint Workspace, client Lync, carte de visite dans toutes les applications clientes Office et volet personnes dans Outlook  <br/> |Volet personnes dans Outlook  <br/> |
|Authentification de base  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification basée sur les formulaires  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification mise en cache  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation mise en cache des amis vers le dossier contacts dans la Banque par défaut  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation des activités mises en cache pour les amis sur le dossier d' **échange de News** masqué  <br/> |Non  <br/> |Oui  <br/> |
|Synchronisation à la demande (image, nom, titre) pour des amis et des non-amis sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Activités à la demande synchronisées pour les amis et les non-amis sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Suivre sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Ne pas suivre sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Visiter la page de profil utilisateur  <br/> |Via un lien  <br/> |Via un badge réseau  <br/> |
|Observation des paramètres de confidentialité sur le réseau social (par exemple, affichage du profil et des activités des non Friends qui permettent d'afficher ces informations)  <br/> |Oui  <br/> |Oui  <br/> |
|Adresses de messagerie hachées transmises au fournisseur  <br/> |Oui  <br/> |Oui  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Modifications de la version précédente de l'extensibilité du fournisseur OSC

Le tableau suivant montre les membres qui ont été ajoutés ou déconseillés à partir de l'interface correspondante.
  
|**Interface et membre**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |DéConseillée dans Outlook Social Connector 2013. Notez que **ISocialSession:: GetActivities** a également été déconseillé depuis Outlook Social Connector 1,1.  <br/> Pour synchroniser les flux d'activités, vous devez implémenter la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **dynamicActivitiesLookupEx** comme **true**, ce qui entraîne l'invite de la propriété OSC à appeler **ISocialSession2:: GetActivitiesEx** .  <br/> |
   
Le tableau suivant présente les éléments de schéma qui ont été modifiés.
  
|**Élément de schéma**|**Comment**|
|:-----|:-----|
|**possibilités** <br/> |Ajouté dans Outlook Social Connector 2013: élément **allowChangesToAutoConfigure** .  <br/> DéConseillée dans Outlook Social Connector 2013: élément **cacheActivities** .  <br/> |
|**person** <br/> |Ajouté dans Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **Interests**, ** emplacement**, **OtherAddress,**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **compétences**, **écoles**et éléments de **site Web** .  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [XML pour les amis](xml-for-friends.md)
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

