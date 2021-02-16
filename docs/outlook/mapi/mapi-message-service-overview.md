---
title: Vue d’ensemble du service de message MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406254"
---
# <a name="mapi-message-service-overview"></a>Vue d’ensemble du service de message MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un service de messagerie définit un groupe de fournisseurs de services associés, généralement des fournisseurs de services qui fonctionnent avec le même système de messagerie. Tandis que les fournisseurs de services effectuent le travail de communication entre les systèmes de messagerie et le sous-système MAPI, les services de messagerie effectuent le travail d’interconnexion entre l’utilisateur et les fournisseurs de services qui fonctionnent avec un système de messagerie commun.  
  
Des services de messagerie existent pour faciliter l’installation et la configuration des fournisseurs de services pour les utilisateurs. Les utilisateurs n’installent jamais ou ne configurent jamais directement un fournisseur de services . le service de messagerie gère entièrement l’installation et la configuration de chacun des fournisseurs de services qui appartiennent au service. En raison de cette fonctionnalité, les utilisateurs n’ont pas besoin de connaître les exigences de configuration spécifiques du fournisseur de services. 
  
La figure suivante illustre la relation entre une application cliente basée sur la messagerie et deux services de messagerie.
  
**Installation et configuration du service de messagerie**
  
![Installation et configuration du service de message et configuration]du service de(media/amapi_44.gif "message")
  
L’utilisateur appelle le code d’installation de chaque service de messagerie pour ajouter le service et ses fournisseurs de services à un profil. Dans l’un des services de messagerie illustrés dans la figure, il existe trois fournisseurs de services ; dans l’autre service de messagerie, il existe deux fournisseurs de services. Une fois l’installation terminée, généralement au moment de l’installation, les fournisseurs de services de chaque service de messagerie sont configurés. Le code de configuration de chaque service de message gère la configuration des fournisseurs dans le service.
  
Lorsqu’un service de message est installé, son programme d’installation copie les fichiers nécessaires de la source d’installation sur le disque local de l’utilisateur et met à jour un fichier de configuration, Mapisvc.inf. Le fichier Mapisvc.inf contient les paramètres de configuration de tous les services de messagerie et fournisseurs de services qui peuvent être installés sur l’ordinateur. Il est organisé en sections hiérarchiques, avec des liens entre chaque section à chaque niveau. La section au niveau supérieur contient des informations pertinentes pour le sous-système MAPI, telles qu’une liste de tous les services de message disponibles et pour l’installation de l’aide en ligne. Le niveau suivant contient des sections pour chaque service de message, avec des informations telles que le nom de fichier DLL du service de message et le nom de sa fonction de point d’entrée de configuration. Le troisième niveau contient des sections avec des données de configuration pour chaque fournisseur de services dans le service de messagerie. 
  
Pour gérer la configuration, un service de message implémente une fonction de point d’entrée conforme à un prototype défini par MAPI et une boîte de dialogue à onglets appelée feuille de propriétés. MAPI appelle la fonction de point d’entrée pour les demandes clientes de service liées à la gestion des profils et à la gestion des fournisseurs de services dans le service de messagerie. Les feuilles de propriétés sont utilisées pour afficher et modifier les propriétés de configuration du service de messagerie et du fournisseur de services. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

