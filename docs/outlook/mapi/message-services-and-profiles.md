---
title: Profils et des services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 60a102a68ee11cd6002be9edf47d0cee93ed2e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581432"
---
# <a name="message-services-and-profiles"></a>Profils et des services de messagerie
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certains utilisateurs requièrent les services de plusieurs systèmes de messagerie, chacun avec un ou plusieurs fournisseurs de services. Car il est difficile à installer et configurer individuellement chacun de ces fournisseurs de services, car un serveur de messagerie nécessite généralement un groupe de fournisseurs associés pour exposer toutes ses fonctionnalités, MAPI inclut le concept d’un service de message. Services de messagerie aident les utilisateurs à installer et configurer leurs fournisseurs de services.
  
Pour créer un service de message, un développeur écrit un programme de point d’entrée du service de message pour gérer la configuration de chaque fournisseur dans le service et un programme d’installation pour effectuer les opérations suivantes :
  
- Installer le service de chaque fournisseur.
    
- Créer les entrées du fichier de Registre et initialisation.
    
- Créer des entrées dans le fichier de configuration MAPI Mapisvc.inf.
    
Le fichier Mapisvc.inf contient des informations relatives à la configuration de tous les services de messagerie et les fournisseurs de services installés sur l’ordinateur. Il se compose des sections hiérarchiques, avec chaque niveau de lié à la suivante. Dans la partie supérieure sont trois sections qui contiennent les éléments suivants : 
  
- Liste des fichiers d’aide de service de message.
    
- Une liste des services de message plus importantes, ou par défaut.
    
- Une liste de tous les services sur l’ordinateur.
    
Le niveau suivant contient des sections pour chaque service de message et le dernier niveau contient des sections pour chaque fournisseur de services dans un service. MAPI exige que les développeurs de fournisseurs de services et les services de messagerie ajoutent certaines entrées à Mapisvc.inf ; les développeurs peuvent ajouter d’autres entrées à leur convenance. La plupart des informations de Mapisvc.inf finit dans un ou plusieurs profils, une collection d’informations de configuration pour un utilisateur préféré ensemble de services de messagerie. Un ordinateur peut avoir plusieurs utilisateurs et un utilisateur unique peut avoir plusieurs ensembles de préférences, plusieurs profils peuvent exister sur un ordinateur. Chaque profil décrit un ensemble de services de messagerie différent. Avoir plusieurs profils permet à un utilisateur à l’utilisation, par exemple, chez un ensemble de services de messagerie et au bureau avec un ensemble différent.
  
Profils créés à l’installation du service de message ou l’heure d’ouverture de session par une application cliente qui fournit la prise en charge de la configuration. MAPI fournit deux clients de ces applications : un élément du Panneau de configuration et l’Assistant profil. L’élément du Panneau de configuration est une application de la configuration complète avec lequel les utilisateurs peuvent créer, supprimer, modifier et copier des profils, ainsi qu’apporter des modifications aux entrées situées dans un profil. L’Assistant profil est une simple application conçue pour faciliter l’ajout d’un service de message à un profil aussi simple que possible. L’Assistant profil se compose d’une série de boîtes de dialogue, appelée pages de propriétés, qui invite l’utilisateur à travers le processus d’installation et configuration d’un service. L’utilisateur est invité uniquement pour les valeurs pour les paramètres stratégiques ; tous les autres paramètres héritent des valeurs par défaut. Une fois que le profil a été créé, les utilisateurs ne sont pas autorisés à apporter des modifications. 
  
Tandis que l’élément du Panneau de configuration est toujours appelé par le biais du Panneau de configuration, il existe de nombreux scénarios qui peuvent provoquer l’Assistant profil à appeler. Les applications clientes peuvent appeler l’Assistant profil pour créer un profil par défaut au moment de l’ouverture de session lorsqu’un n'a pas encore été créé. Au lieu de réimplémenter le code pour ajouter un profil, l’élément du Panneau de configuration ou une autre application cliente permettre compter sur les fonctionnalités déjà dans l’Assistant profil. Un service de message, en fonction de son point d’entrée, peut appeler l’Assistant profil lorsque le service doit être ajouté au profil par défaut. Services de messagerie qui utilisent l’Assistant profil doivent écrire une fonction de point d’entrée supplémentaire et une procédure de boîte de dialogue Windows standard. L’Assistant profil appelle la fonction de point d’entrée pour récupérer la boîte de dialogue configuration du service pendant la procédure de boîte de dialogue gère les messages qui sont générées lorsque cette boîte de dialogue est en cours d’utilisation. 
  
Les profils sont organisés de façon similaire au fichier Mapisvc.inf. Profils ont liés sections hiérarchiques ; service fournisseurs propres sections de niveau le plus bas, services message possèdent des sections de niveau intermédiaire et MAPI possède des sections de niveau le plus élevé. Chaque section est identifiée par un identificateur unique appelé une [MAPIUID](mapiuid.md). Les sections MAPI contiennent des informations internes à MAPI, tels que les identificateurs de toutes les sections de profil de service de message et des liens vers chacune des autres sections. Chaque section du service de message stocke des liens vers les sections de fournisseur, et chaque section fournisseur stocke un lien vers la section service. 
  
L’illustration suivante montre le contenu des deux profils standard. SAM a deux profils sur son ordinateur, un pour un usage personnel et un pour l’utilisation d’office. Le profil d’accueil contient trois services de messagerie. Message Service X est un service de fournisseur unique pour la gestion de carnet d’adresses. Message Services Y et Z comporte trois fournisseurs : un fournisseur de carnet d’adresses, un fournisseur de magasin de message et un fournisseur de transport. Profil de travail de SAM contient deux services différents de messages, chacun d'entre eux avec un fournisseur de carnet d’adresses, d’un fournisseur de magasin de message et un fournisseur de transport. 
  
**Exemple de profil**
  
![Exemple de profil] (media/amapi_56.gif "Exemple de profil")
  
L’illustration suivante montre un profil qui inclut deux services de messagerie. Le code pour installer et configurer les fournisseurs de services qui appartiennent au service de message se trouve dans la même DLL que le code pour les fournisseurs. Ce code lit les informations de profil au moment de l’ouverture de session pour configurer les fournisseurs de services, et il invite l’utilisateur, dans la mesure du possible et nécessaire, les informations manquantes. Demandes d’un client pour afficher ou modifier les paramètres de configuration pour tous les fournisseurs sont également gérés par ce code courantes.
  
**Installation et configuration des fournisseurs de services**
  
![Installation et configuration des fournisseurs de services] (media/amapi_55.gif "Installation et configuration des fournisseurs de services")
  
## <a name="see-also"></a>Voir aussi

- [MAPIUID](mapiuid.md)
- [Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)

