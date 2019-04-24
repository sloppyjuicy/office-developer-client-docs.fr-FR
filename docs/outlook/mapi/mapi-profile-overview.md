---
title: Vue d'ensemble du profil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328162"
---
# <a name="mapi-profile-overview"></a>Vue d'ensemble du profil MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un profil est une collection d'informations sur les services de messagerie et les fournisseurs de services qu'un utilisateur d'une application cliente souhaite être disponible au cours d'une session MAPI particulière. Chaque utilisateur possède au moins un profil; de nombreux utilisateurs en ont toujours plusieurs. Par exemple, un utilisateur peut avoir un profil à utiliser avec un service de banque de messages basé sur un serveur et un autre pour travailler avec un service de banque de messages sur l'ordinateur local. Un utilisateur peut accéder à un ensemble de systèmes de messagerie en utilisant les services de transport appropriés pour une partie de la journée et un autre pour le reste de la journée. Les profils permettent de sélectionner des combinaisons de services de système de messagerie. 
  
Le nom des profils peut contenir jusqu'à 64 caractères alphanumériques. Les noms peuvent inclure des caractères d'accentuation, le trait de soulignement et les espaces incorporés, et ne peuvent pas contenir d'espaces de début ou de fin. 
  
Les profils sont organisés de façon hiérarchique et sont divisés en sections, avec une section pour chaque service de messagerie et une section pour chaque fournisseur de services dans un service. Les sections associées sont liées, ce qui facilite la navigation dans les informations. Chaque section contient une série d'entrées que MAPI ou une application cliente utilise pour la configuration.
  
Les entrées incluses dans un profil varient en fonction du service de messagerie vers le service de messagerie. Voici quelques entrées communes:
  
- Nom de chaque service de messagerie ou fournisseur de services.
    
- Le nom des dll qui contiennent les fournisseurs de services et les services de messagerie.
    
- Nom de la fonction de point d'entrée de chaque service de messagerie.
    
- Une liste des fournisseurs de services qui composent chaque service de messagerie.
    
Des profils peuvent être créés lors de l'installation, lorsque MAPI ou un service de messagerie est chargé sur un ordinateur, ou ultérieurement. MAPI fournit l'Assistant Profil pour l'administration des profils. 
  
L'Assistant Profil est une application qui crée des profils avec un volume de travail minimal. L'Assistant utilise les valeurs par défaut des paramètres dans la mesure du possible, ce qui permet aux utilisateurs d'économiser du temps et de l'énergie. Les utilisateurs ne peuvent entrer des valeurs qu'en cas d'absolue nécessité. Pour plus d'informations, consultez [la rubrique Création d'un profil à l'aide de l'Assistant Profil](creating-a-profile-by-using-the-profile-wizard.md). Vous pouvez également utiliser l'outil de personnalisation Office pour créer un nouveau profil. Pour plus d’informations, voir [Outil de personnalisation Office](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Voir aussi



[Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

