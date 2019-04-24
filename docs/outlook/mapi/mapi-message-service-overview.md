---
title: Vue d'ensemble du service de messagerie MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345978"
---
# <a name="mapi-message-service-overview"></a>Vue d'ensemble du service de messagerie MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un service de messagerie définit un groupe de fournisseurs de services associés, généralement des fournisseurs de services qui fonctionnent avec le même système de messagerie. Tandis que les fournisseurs de services effectuent le travail de communication entre les systèmes de messagerie et le sous-système MAPI, les services de messagerie effectuent le travail d'interfaçage entre l'utilisateur et les fournisseurs de services qui fonctionnent avec un système de messagerie commun.  
  
Il existe des services de messagerie pour faciliter l'installation et la configuration des fournisseurs de services. Les utilisateurs ne peuvent jamais installer ou configurer directement un fournisseur de services; le service de messagerie gère entièrement l'installation et la configuration de chacun des fournisseurs de services appartenant au service. En raison de cette fonctionnalité, les utilisateurs n'ont pas besoin de se familiariser avec les exigences de configuration de fournisseurs de services spécifiques. 
  
La figure suivante illustre la relation entre une application cliente basée sur la messagerie et deux services de message.
  
**Installation et configuration du service de messagerie**
  
![Installation et configuration du service de messagerie] (media/amapi_44.gif "Installation et configuration du service de messagerie")
  
L'utilisateur appelle le code d'installation de chaque service de messagerie pour ajouter le service et ses fournisseurs de services à un profil. Dans l'un des services de message indiqués dans la figure, il existe trois fournisseurs de services; dans l'autre service de messagerie, il existe deux fournisseurs de services. Plus tard, une fois l'installation terminée, généralement à l'ouverture de session, les fournisseurs de services de chaque service de messagerie sont configurés. Le code de configuration de chaque service de messagerie gère la configuration des fournisseurs dans le service.
  
Lorsqu'un service de messagerie est installé, son programme d'installation copie les fichiers nécessaires de la source d'installation sur le disque local de l'utilisateur et met à jour un fichier de configuration, MAPISVC. inf. Le fichier MAPISVC. INF contient les paramètres de configuration de tous les services de messagerie et fournisseurs de services qui peuvent être installés sur l'ordinateur. Elle est organisée en sections hiérarchiques, avec des liens entre chaque section à chaque niveau. La section au niveau supérieur contient des informations pertinentes pour le sous-système MAPI, telles que la liste de tous les services de messagerie disponibles, ainsi que l'installation de l'aide en ligne. Le niveau suivant comporte des sections pour chaque service de messagerie, avec des informations telles que le nom du fichier DLL du service de messagerie et le nom de sa fonction de point d'entrée de configuration. Le troisième niveau comporte des sections avec des données de configuration pour chaque fournisseur de services dans le service de messagerie. 
  
Pour gérer la configuration, un service de messagerie implémente une fonction de point d'entrée conforme à un prototype défini par MAPI, ainsi qu'une boîte de dialogue avec onglets appelée feuille de propriétés. MAPI appelle la fonction de point d'entrée pour traiter les demandes client qui se rapportent à la gestion des profils et la gestion des fournisseurs de services dans le service de messagerie. Les feuilles de propriétés sont utilisées pour afficher et modifier les propriétés de configuration du service de messagerie et du fournisseur de services. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

