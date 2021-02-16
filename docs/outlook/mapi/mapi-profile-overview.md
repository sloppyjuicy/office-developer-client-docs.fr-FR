---
title: Vue d’ensemble du profil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328162"
---
# <a name="mapi-profile-overview"></a>Vue d’ensemble du profil MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un profil est une collection d’informations sur les services de messagerie et les fournisseurs de services qu’un utilisateur d’une application cliente souhaite rendre disponibles au cours d’une session MAPI particulière. Chaque utilisateur possède au moins un profil . de nombreux utilisateurs en conservent plusieurs. Par exemple, un utilisateur peut avoir un profil pour travailler avec un service de magasin de messages basé sur un serveur et un autre profil pour travailler avec un service de magasin de messages sur l’ordinateur local. Un utilisateur peut vouloir accéder à un ensemble de systèmes de messagerie en utilisant les services de transport appropriés pour une partie de la journée et un autre ensemble pour le reste de la journée. Les profils offrent un moyen flexible de sélectionner des combinaisons de services système de messagerie. 
  
Les profils peuvent avoir jusqu’à 64 caractères alphanumériques. Les noms peuvent inclure des caractères d’accentuation, le trait de soulignement et des espaces incorporés, et ne peuvent pas inclure d’espaces de début ou de fin. 
  
Les profils sont organisés hiérarchiquement et divisés en sections, avec une section pour chaque service de messagerie et une section pour chaque fournisseur de services dans un service. Les sections associées sont liées, ce qui facilite la navigation dans les informations. Chaque section contient une série d’entrées que MAPI ou une application cliente utilise pour la configuration.
  
Les entrées incluses dans un profil varient d’un service de message à l’autre. Voici quelques-unes des entrées courantes :
  
- Nom de chaque service de messagerie ou fournisseur de services.
    
- Nom des DLLs qui contiennent des fournisseurs de services et des services de messagerie.
    
- Nom de la fonction de point d’entrée de chaque service de message.
    
- Liste des fournisseurs de services qui font chaque service de messagerie.
    
Les profils peuvent être créés au moment de l’installation, lorsque MAPI ou un service de message est chargé sur un ordinateur, ou à tout moment ultérieur. MAPI fournit l’Assistant Profil pour l’administration des profils. 
  
L’Assistant Profil est une application qui crée de nouveaux profils avec un minimum de travail. Dans la mesure du possible, l’Assistant utilise les valeurs par défaut pour les paramètres, ce qui permet aux utilisateurs de gagner du temps et de l’effort. Les utilisateurs entrent des valeurs uniquement lorsque cela est absolument nécessaire. Pour plus d’informations, [voir Création d’un profil à l’aide de l’Assistant Profil.](creating-a-profile-by-using-the-profile-wizard.md) Vous pouvez également utiliser l’Outil de personnalisation Office pour créer un profil. Pour plus d’informations, voir [Outil de personnalisation Office](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

