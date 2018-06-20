---
title: Nouveautés pour les fournisseurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Cette rubrique répertorie les principales modifications apportées dans Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1.1.
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787724"
---
# <a name="whats-new-for-providers"></a>Nouveautés pour les fournisseurs

Cette rubrique répertorie les principales modifications apportées dans Outlook Social Connector 2013 (OSC). Il présente une comparaison des fonctionnalités disponibles entre Outlook Social Connector 2013 et Outlook Social Connector 1.1. Il décrit également des membres de l’interface et les éléments XML qui ont été ajoutées, modifiées ou déconseillées. 
  
Dans Office 2013, l’OSC fonctionne avec non seulement Outlook, mais également SharePoint Server, SharePoint Workspace, client Lync et tous les autres Office des applications clientes qui prennent en charge les informations de présence et de la carte de visite. Un fournisseur OSC peut faire apparaître les mises à jour des informations de mise sous l’onglet **What ' s NEW** dans le volet personnes Outlook, ainsi que dans la carte de visite. 
  
Quelques modifications majeures dans Outlook Social Connector 2013 sont les suivantes : 
  
- Si un fournisseur prend en charge affichant les activités, le fournisseur toujours synchronise les activités à la demande et n’est plus sur activités précédemment mis en cache. Cela signifie que le fournisseur stocke les activités des amis et non amis en mémoire pour afficher les activités de la plus récentes.
    
- Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs via Internet doivent utiliser le protocole HTTPS (Hypertext Transfer Protocol (HTTP) avec Secure Socket Layer (SSL)). Dans le cas contraire, il existe un risque que les adresses de messagerie, les activités de réseaux sociaux et autres utilisateurs interceptées ou exposées en cours de transfert de données.
    
- Si vous avez des fournisseurs fonctionnant avec une version antérieure d’Outlook, pour prendre en charge d’Office 2013, vous devez mettre à jour le package d’installation. Pour plus d’informations, voir [Installation Checklist](installation-checklist.md) . 
    
Le tableau suivant indique la disponibilité des différentes fonctionnalités dans Outlook Social Connector 2013 par rapport à Outlook Social Connector 1.1.
  
|**Fonctionnalité**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interface utilisateur final  <br/> |SharePoint Server, SharePoint Workspace, client Lync, carte de visite dans toutes les applications clientes d’Office et le volet personnes dans Outlook  <br/> |Volet personnes dans Outlook  <br/> |
|Authentification de base  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification basée sur les formulaires  <br/> |Oui  <br/> |Oui  <br/> |
|Authentification mise en cache  <br/> |Oui  <br/> |Oui  <br/> |
|Stocker mis en cache de synchronisation pour vos amis au dossier contacts par défaut  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation des activités mis en cache pour amis au dossier **d’échange de News** masqué  <br/> |Non  <br/> |Oui  <br/> |
|Synchronisation de la demande (image, name, titre) d’amis ou non amis sur réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Synchronisation des activités à la demande d’amis ou non amis sur réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Suivre sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Ne suivent pas sur le réseau  <br/> |Oui  <br/> |Oui  <br/> |
|Visitez la page de profil utilisateur  <br/> |Par le biais d’un lien  <br/> |Par le biais d’une étiquette de réseau  <br/> |
|Observation des paramètres de confidentialité sur un réseau social (par exemple, affichage profil et non-amis autoriser l’affichage de ces activités)  <br/> |Oui  <br/> |Oui  <br/> |
|Adresses de messagerie de hachage passé au fournisseur  <br/> |Oui  <br/> |Oui  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Modifications de la version précédente de l’extensibilité de fournisseur OSC

Le tableau suivant indique les membres qui ont été ajoutés ou déconseillées à partir de l’interface correspondante.
  
|**Interface et le membre**|**Commentaire**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Obsolète dans Outlook Social Connector 2013. Notez que **ISocialSession::GetActivities** a également été déconseillée depuis Outlook Social Connector 1.1.  <br/> Pour synchroniser les informations sur les activités, vous devez implémenter la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **dynamicActivitiesLookupEx** comme **true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.  <br/> |
   
Le tableau suivant indique les éléments de schéma qui ont été modifiés.
  
|**Élément de schéma**|**Commentaire**|
|:-----|:-----|
|**fonctionnalités** <br/> |Ajouté dans Outlook Social Connector 2013 : élément **allowChangesToAutoConfigure** .  <br/> Déconseillées dans Outlook Social Connector 2013 : élément **cacheActivities** .  <br/> |
|**person** <br/> |Ajouté dans Outlook Social Connector 2013 : **askmeabout**, **businessAddress**, **Ville (bureau)**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **centres d’intérêt**, ** emplacement**, éléments **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **compétences**, **écoles**et **site Web** .  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Code XML des amis](xml-for-friends.md)
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

