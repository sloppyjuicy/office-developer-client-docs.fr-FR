---
title: Vue d’ensemble du service de message MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fc444725aae20e7321fa287a90cf7d3e13b7ffb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784633"
---
# <a name="mapi-message-service-overview"></a>Vue d’ensemble du service de message MAPI
  
**S’applique à**: Outlook 
  
Un service de message définit un groupe de fournisseurs de service associé, généralement des fournisseurs de services qui fonctionnent avec le même système de messagerie. Tandis que les fournisseurs de services exécutent le travail de communication entre les systèmes de messagerie et le sous-système MAPI, services message les tâches d’interface entre les fournisseurs de services qui fonctionnent avec un système de messagerie courants.  
  
Services de messagerie existent pour simplifier l’installation et la configuration des fournisseurs de services pour les utilisateurs. Les utilisateurs ne jamais directement installer ou configurer un fournisseur de services ; le service de message gère complètement l’installation et la configuration de chacun des fournisseurs de services qui appartiennent au service. En raison de cette fonctionnalité, les utilisateurs est inutile de se familiariser avec les exigences de configuration de fournisseur de service spécifiques. 
  
La figure suivante illustre la relation entre une application cliente basée sur la messagerie et de deux services de messagerie.
  
**Configuration et installation du service de message**
  
![Configuration et installation du service de message] (media/amapi_44.gif "Configuration et installation du service de message")
  
L’utilisateur appelle le code d’installation de chaque service de message pour ajouter le service et ses fournisseurs de service à un profil. Dans un des services de message illustrés dans la figure, il existe trois fournisseurs de services ; dans l’autre service de message, il existe deux fournisseurs de services. Ultérieurement une fois l’installation terminée, généralement au moment de l’ouverture de session, les fournisseurs de services dans chaque service de message sont configurés. Le code de configuration dans le service de chaque message gère la configuration des fournisseurs dans le service.
  
Lorsqu’un service de message est installé, son programme d’installation copie les fichiers nécessaires à partir de la source d’installation sur le disque local de l’utilisateur et met à jour un fichier de configuration, Mapisvc.inf. Le fichier Mapisvc.inf contient les paramètres de configuration de l’ensemble des services de messagerie et des fournisseurs de services qui peuvent être installés sur l’ordinateur. Il se compose des sections hiérarchiques, avec des liens entre chaque section à chaque niveau. La section au niveau supérieur contient des informations qui sont pertinentes pour le sous-système MAPI, telle qu’une liste de tous les services de message disponibles et pour l’installation d’aide en ligne. Le niveau suivant comporte des sections pour chaque service de message, avec des informations telles que le nom du fichier DLL du service message et le nom de la fonction de point d’entrée de sa configuration. Le troisième niveau comporte des sections avec des données de configuration pour chaque fournisseur de service dans le service de message. 
  
Pour gérer la configuration, un service de message implémente une fonction de point d’entrée est conforme à un prototype défini par MAPI et une boîte de dialogue à onglets appelé une feuille de propriétés. MAPI appelle la fonction de point d’entrée pour les demandes des clients qui sont associées à la gestion des profils et la gestion des fournisseurs de services dans le service de message. Feuilles de propriétés sont utilisées pour l’affichage et modification des propriétés de configuration de fournisseur de service service de message. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

