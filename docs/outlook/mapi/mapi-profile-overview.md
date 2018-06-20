---
title: Vue d’ensemble des profils MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 573709c4374786bb1bd3d763c8ba91de59f7fb1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784651"
---
# <a name="mapi-profile-overview"></a>Vue d’ensemble des profils MAPI

  
  
**S’applique à**: Outlook 
  
Un profil est une collection d’informations sur les services de messagerie et les fournisseurs de services qu’un utilisateur d’une application cliente souhaite soit disponible pendant une session MAPI spécifique. Chaque utilisateur dispose d’au moins un profil ; nombre d’utilisateurs conserver plusieurs. Par exemple, un utilisateur peut avoir un profil pour fonctionner avec un service de banque de messages sur le serveur et un autre profil pour fonctionner avec un service de banque de messages sur l’ordinateur local. Un utilisateur souhaite accéder à un ensemble de systèmes de messagerie à l’aide des services de transport approprié pour une partie de la journée et un autre pour le reste de la journée. Les profils fournissent une grande souplesse pour sélectionner des combinaisons de services de système de messagerie. 
  
Profils peuvent contenir jusqu'à 64 caractères alphanumériques, les noms de longueur. Les noms peuvent inclure des caractères d’accentuation, le trait de soulignement et des espaces et ne peut pas contenir d’espaces de début ou de fin. 
  
Les profils sont organisées de façon hiérarchique et divisés en sections, avec une section pour chaque service de message et une section pour chaque fournisseur de services dans un service. Les sections connexes sont liées, ce qui facilite parcourir les informations. Chaque section contient une série d’entrées MAPI ou une application cliente utilise pour la configuration.
  
Les entrées incluses dans un profil varient à partir du service de message au service de message. Certaines entrées courantes sont les suivantes :
  
- Le nom de chaque service de message ou d’un fournisseur de services.
    
- Nom des DLL qui contiennent des fournisseurs de services et services de message.
    
- Nom de la fonction de point d’entrée du service de chaque message.
    
- Liste des fournisseurs de services qui constituent le service de chaque message.
    
Profils peuvent être créés au moment de l’installation, lorsque MAPI ou un service de message est chargé sur un ordinateur, ou ultérieurement. MAPI propose l’Assistant profil pour l’administration des profils. 
  
L’Assistant profil est une application qui crée des profils avec un minimum de travail. L’Assistant utilise le valeurs par défaut pour les paramètres dans la mesure du possible, l’enregistrement d’effort et l’heure d’utilisateurs. Les utilisateurs entrent des valeurs uniquement lorsque cela est nécessaire. Pour plus d’informations, consultez [Création d’un profil à l’aide de l’Assistant profil](creating-a-profile-by-using-the-profile-wizard.md). Vous pouvez également utiliser l’outil de personnalisation Office pour créer un nouveau profil. Pour plus d’informations, voir [Outil de personnalisation Office](http://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Voir aussi



[Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

