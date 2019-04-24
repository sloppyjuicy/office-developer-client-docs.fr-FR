---
title: Profils et services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 78a13bacf13b019bbf9436830ad66db7fdfaf425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356957"
---
# <a name="message-services-and-profiles"></a>Profils et services de messagerie
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains utilisateurs ont besoin des services de plusieurs systèmes de messagerie, chacun avec un ou plusieurs fournisseurs de services. Étant donné qu'il est lourd d'installer et de configurer chacun de ces fournisseurs de services individuellement, et qu'un serveur de messagerie exige généralement un groupe de fournisseurs associés pour exposer toutes ses fonctionnalités, MAPI inclut le concept de service de messagerie. Les services de messagerie aident les utilisateurs à installer et à configurer leurs fournisseurs de services.
  
Pour créer un service de messagerie, un développeur écrit un programme de point d'entrée de service de message afin de gérer la configuration de chaque fournisseur du service et d'un programme d'installation pour effectuer les opérations suivantes:
  
- Installez chaque fournisseur dans le service.
    
- Créez des entrées de Registre et de fichier d'initialisation.
    
- Créez des entrées dans le fichier de configuration MAPI, MAPISVC. inf.
    
Le fichier MAPISVC. INF contient des informations relatives à la configuration de tous les services de messagerie et fournisseurs de services installés sur l'ordinateur. Elle est organisée en sections hiérarchiques, chaque niveau étant lié à la suivante. Les deux sections suivantes contiennent les éléments suivants: 
  
- Liste des fichiers d'aide du service de messagerie.
    
- Une liste des services de messagerie les plus importants ou par défaut.
    
- Liste de tous les services sur l'ordinateur.
    
Le niveau suivant contient des sections pour chaque service de messagerie, et le dernier niveau contient des sections pour chaque fournisseur de services dans un service. MAPI exige que les développeurs de fournisseurs de services et de services de messagerie ajoutent certaines entrées à Mapisvc. inf; les développeurs peuvent ajouter d'autres entrées à leur propre discrétion. La plupart des informations contenues dans le fichier MAPISVC. inf se terminent dans un ou plusieurs profils, une collection d'informations de configuration pour l'ensemble privilégié des services de messagerie d'un utilisateur. Étant donné qu'un ordinateur peut avoir plusieurs utilisateurs et qu'un seul utilisateur peut avoir plusieurs ensembles de préférences, de nombreux profils peuvent exister sur un ordinateur. Chaque profil décrit un ensemble différent de services de messagerie. Le fait de disposer de plusieurs profils permet à un utilisateur de travailler, par exemple, à la maison avec un ensemble de services de messagerie et au bureau avec un ensemble différent.
  
Les profils sont créés lors de l'installation du service de messagerie ou de l'ouverture de session par une application cliente qui fournit la prise en charge de la configuration. MAPI fournit deux applications clientes de ce type: un élément du panneau de configuration et l'Assistant Profil. L'élément du panneau de configuration est une application de configuration de service complet avec laquelle les utilisateurs peuvent créer, supprimer, modifier et copier des profils, ainsi que modifier les entrées d'un profil. L'Assistant Profil est une application simple conçue pour faciliter l'ajout d'un service de messagerie à un profil. L'Assistant Profil se compose d'une série de boîtes de dialogue, appelées pages de propriétés, qui invitent l'utilisateur à passer par le processus d'installation et de configuration d'un service. L'utilisateur est invité uniquement à indiquer les valeurs des paramètres les plus critiques; tous les autres paramètres héritent des valeurs par défaut. Une fois le profil créé, les utilisateurs ne sont pas autorisés à effectuer des modifications. 
  
Tandis que l'élément du panneau de configuration est toujours appelé dans le panneau de configuration, il existe un grand nombre de scénarios susceptibles d'entraîner l'appel de l'Assistant Profil. Les applications clientes peuvent appeler l'Assistant Profil pour créer un profil par défaut lors de l'ouverture de session lorsque l'utilisateur n'a pas encore été créé. Au lieu d'implémenter le code pour ajouter un profil, l'élément du panneau de configuration ou une autre application cliente peut compter sur les fonctionnalités déjà présentes dans l'Assistant Profil. Un service de messagerie, dans sa fonction de point d'entrée, peut appeler l'Assistant Profil lorsque le service doit être ajouté au profil par défaut. Les services de messagerie qui utilisent l'Assistant Profil doivent écrire une fonction de point d'entrée supplémentaire et une procédure de boîte de dialogue Windows standard. L'Assistant Profil appelle la fonction de point d'entrée pour récupérer la boîte de dialogue de configuration du service tandis que la procédure de la boîte de dialogue gère les messages générés lorsque cette boîte de dialogue est en cours d'utilisation. 
  
Les profils sont organisés de la même façon que le fichier MAPISVC. inf. Les profils ont des sections hiérarchiques liées; les fournisseurs de services possèdent des sections au niveau le plus bas, les sections des services de messagerie au niveau intermédiaire et MAPI, le niveau le plus élevé. Chaque section est identifiée par un identificateur unique appelé [MAPIUID](mapiuid.md). Les sections MAPI contiennent des informations internes à MAPI, telles que les identificateurs de toutes les sections de profil de service de message et des liens vers chacune des autres sections. Chaque section service de messagerie stocke des liens vers ses sections de fournisseur, et chaque section de fournisseur stocke un lien vers sa section service. 
  
L'illustration suivante montre le contenu de deux profils standard. Sam dispose de deux profils sur son ordinateur, un pour les particuliers et un pour l'utilisation d'Office. Le profil d'accueil contient trois services de messagerie. Le service de messagerie X est un service de fournisseur unique pour la gestion des carnets d'adresses. Les services de messagerie Y et Z ont trois fournisseurs, un fournisseur de carnets d'adresses, un fournisseur de banque de messages et un fournisseur de transport. Le profil de travail de Sam contient deux services de messagerie différents, chacun d'eux disposant d'un fournisseur de carnet d'adresses, d'un fournisseur de banque de messages et d'un fournisseur de transport. 
  
**Exemple de profil**
  
![Exemple de profil] (media/amapi_56.gif "Exemple de profil")
  
L'illustration suivante montre un profil qui inclut deux services de messagerie. Le code permettant d'installer et de configurer les fournisseurs de services qui appartiennent au service de messagerie réside dans la même DLL que le code des fournisseurs. Ce code lit les informations du profil au moment de l'ouverture de session pour configurer les fournisseurs de services, et il invite l'utilisateur, si possible et nécessaire, pour les informations manquantes. Les demandes d'un client permettant d'afficher ou de modifier les paramètres de configuration de l'un des fournisseurs sont également gérées par ce code commun.
  
**Installation et configuration des fournisseurs de services**
  
![Installation et configuration des fournisseurs de services] (media/amapi_55.gif "Installation et configuration des fournisseurs de services")
  
## <a name="see-also"></a>Voir aussi

- [MAPIUID](mapiuid.md)
- [Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)

