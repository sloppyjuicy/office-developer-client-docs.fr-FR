---
title: Profils et services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f8f081ea35241f3e57a8cf2345254d24c5032fdc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592052"
---
# <a name="message-services-and-profiles"></a>Profils et services de messagerie
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains utilisateurs ont besoin des services de plusieurs systèmes de messagerie, chacun avec un ou plusieurs fournisseurs de services. Étant donné qu’il est fastidieux d’installer et de configurer chacun de ces fournisseurs de services individuellement et qu’un serveur de messagerie nécessite généralement un groupe de fournisseurs associés pour exposer toutes ses fonctionnalités, MAPI inclut le concept d’un service de messagerie. Les services de messagerie aident les utilisateurs à installer et à configurer leurs fournisseurs de services.
  
Pour créer un service de messagerie, un développeur écrit un programme de point d’entrée de service de message pour gérer la configuration de chaque fournisseur dans le service et un programme d’installation pour les étapes suivantes :
  
- Installez chaque fournisseur dans le service.
    
- Créez des entrées de fichier de Registre et d’initialisation.
    
- Créez des entrées dans le fichier de configuration MAPI Mapisvc.inf.
    
Le fichier Mapisvc.inf contient des informations liées à la configuration de tous les services de messagerie et fournisseurs de services installés sur l’ordinateur. Il est organisé en sections hiérarchiques, chaque niveau est lié au suivant. En haut, trois sections contiennent les éléments suivants : 
  
- Liste des fichiers d’aide du service de message.
    
- Liste des services de messages les plus importants ou par défaut.
    
- Liste de tous les services sur l’ordinateur.
    
Le niveau suivant contient des sections pour chaque service de messagerie et le dernier niveau contient des sections pour chaque fournisseur de services dans un service. MAPI exige que les développeurs de fournisseurs de services et de services de messagerie ajoutent certaines entrées à Mapisvc.inf ; les développeurs peuvent ajouter d’autres entrées à leur propre discrétion. La plupart des informations de Mapisvc.inf se retrouvent dans un ou plusieurs profils, une collection d’informations de configuration pour l’ensemble préféré de services de message d’un utilisateur. Étant donné qu’un ordinateur peut avoir plusieurs utilisateurs et qu’un seul utilisateur peut avoir plusieurs ensembles de préférences, de nombreux profils peuvent exister sur un ordinateur. Chaque profil décrit un ensemble différent de services de messages. Le fait d’avoir plusieurs profils permet à un utilisateur de travailler, par exemple, à la maison avec un ensemble de services de messages et au bureau avec un autre ensemble.
  
Les profils sont créés au moment de l’installation du service de message ou de l’heure d’accès par une application cliente qui assure la prise en charge de la configuration. MAPI fournit deux applications clientes de ce type : un élément du Panneau de contrôle et l’Assistant Profil. L’élément du Panneau de configuration est une application de configuration de service complet avec laquelle les utilisateurs peuvent créer, supprimer, modifier et copier des profils, et apporter des modifications aux entrées d’un profil. L’Assistant Profil est une application simple conçue pour faciliter l’ajout d’un service de message à un profil. L’Assistant Profil se compose d’une série de boîtes de dialogue, appelées pages de propriétés, qui invitent l’utilisateur à passer par le processus d’installation et de configuration d’un service. L’utilisateur est invité uniquement à obtenir les valeurs des paramètres les plus critiques . tous les autres paramètres héritent des valeurs par défaut. Une fois le profil créé, les utilisateurs ne sont pas autorisés à apporter des modifications. 
  
Alors que l’élément du Panneau de contrôle est toujours appelé par le biais du Panneau de contrôle, il existe plusieurs scénarios qui peuvent provoquer l’appel de l’Assistant Profil. Les applications clientes peuvent appeler l’Assistant Profil pour créer un profil par défaut au moment de l’accès lorsqu’un profil n’a pas encore été créé. Au lieu de réapplémenter du code pour ajouter un profil, l’élément du Panneau de contrôle ou une autre application cliente peut s’appuyer sur les fonctionnalités déjà dans l’Assistant Profil. Un service de message, dans sa fonction de point d’entrée, peut appeler l’Assistant Profil lorsque le service doit être ajouté au profil par défaut. Les services de messages qui utilisent l’Assistant Profil doivent écrire une fonction de point d’entrée supplémentaire et une procédure Windows boîte de dialogue standard. L’Assistant Profil appelle la fonction de point d’entrée pour récupérer la boîte de dialogue de configuration du service tandis que la procédure de la boîte de dialogue gère les messages générés lorsque cette boîte de dialogue est en cours d’utilisation. 
  
Les profils sont organisés de la même manière que le fichier Mapisvc.inf. Les profils ont des sections hiérarchiques liées ; les fournisseurs de services possèdent des sections au niveau le plus bas, les services de messagerie possèdent des sections au niveau intermédiaire et MAPI les sections au niveau le plus élevé. Chaque section est identifiée avec un identificateur unique appelé [MAPIUID](mapiuid.md). Les sections MAPI contiennent des informations internes à MAPI, telles que les identificateurs de toutes les sections de profil de service de message et des liens vers chacune des autres sections. Chaque section du service de messagerie stocke des liens vers ses sections de fournisseur, et chaque section de fournisseur stocke un lien vers sa section de service. 
  
L’illustration suivante montre le contenu de deux profils classiques. Sam possède deux profils sur son ordinateur, un pour l’utilisation à domicile et un pour l’utilisation au bureau. Le profil d’accueil contient trois services de message. Message Service X est un service fournisseur unique pour la gestion des carnets d’adresses. Les services de messagerie Y et Z ont trois fournisseurs : un fournisseur de carnet d’adresses, un fournisseur de magasins de messages et un fournisseur de transport. Le profil professionnel de Sam contient deux services de messagerie différents, chacun d’entre eux possède un fournisseur de carnet d’adresses, un fournisseur de magasins de messages et un fournisseur de transport. 
  
**Exemple de profil**
  
![Exemple de profil](media/amapi_56.gif "Exemple de profil")
  
L’illustration suivante montre un profil qui inclut deux services de message. Le code d’installation et de configuration des fournisseurs de services qui appartiennent au service de messagerie réside dans la même DLL que le code des fournisseurs. Ce code lit les informations du profil au moment de l’accès pour configurer les fournisseurs de services et invite l’utilisateur, si possible et nécessaire, à fournir des informations manquantes. Les demandes d’un client pour afficher ou modifier les paramètres de configuration de l’un des fournisseurs sont également gérées par ce code commun.
  
**Installation et configuration des fournisseurs de services**
  
![Installation et configuration des fournisseurs de services](media/amapi_55.gif "Installation et configuration des fournisseurs de services")
  
## <a name="see-also"></a>Voir aussi

- [MAPIUID](mapiuid.md)
- [Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)

