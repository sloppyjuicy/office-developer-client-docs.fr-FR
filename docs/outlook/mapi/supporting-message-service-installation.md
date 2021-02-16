---
title: Prise en charge de l’installation du service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404700"
---
# <a name="supporting-message-service-installation"></a>Prise en charge de l’installation du service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le programme d’installation de votre service de message doit :
  
1. Copiez les fichiers de service de message, tels que le service de messagerie et les DLLs de fournisseur de services, à partir d’un CD ou d’un disque, vers un lecteur local sur la station de travail. Les fichiers qui doivent être copiés dépendent de votre service de message. En règle générale, vous copiez au moins une DLL.
    
2. Ajoutez des entrées au fichier de configuration Mapisvc.inf. Pour plus d’informations sur la modification de ce fichier pour prendre en charge les fournisseurs de services dans votre service de messagerie, voir Format de fichier [de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Ajoutez, le cas échéant, des entrées au Registre système pour les services de message. Pour plus d’informations sur la façon dont les entrées doivent apparaître dans le Registre système, voir [Installation du sous-système MAPI](installing-the-mapi-subsystem.md).
    
4. Créez un profil par défaut s’il n’en existe pas encore à l’aide de l’un des éléments suivants :
    
  - Assistant Profil pour créer un profil à l’aide de l’interaction utilisateur par le biais d’une série de boîtes de dialogue. Pour plus d’informations sur l’utilisation de l’Assistant Profil, voir [Création d’un profil à l’aide de l’Assistant Profil.](creating-a-profile-by-using-the-profile-wizard.md)
    
  - Panneau de contrôle pour créer un profil à l’aide de l’interaction utilisateur. Le Panneau de configuration offre à l’utilisateur plus de flexibilité que l’Assistant Profil pour la configuration des services de message et la définition des propriétés de profil. 
    
Placez le programme d’installation dans un répertoire public désigné. Ceci est important car la plupart des clients de configuration, tels que le Panneau de configuration, exigent que les utilisateurs entrent le nom de l’annuaire. Le Panneau de configuration appelle un programme  d’installation lorsqu’un utilisateur clique sur le bouton Ajouter, appelle la boîte de dialogue Avoir un disque et spécifie le chemin d’accès au programme.  Le Panneau de contrôle exécute le programme et appelle la fonction de point d’entrée de votre service de message avec le paramètre  _ulContext_ paramétré sur MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Étant donné que les profils font partie intégrante de l’architecture MAPI, assurez-vous que votre programme d’installation ne stocke rien dans le profil par défaut qui serait difficile à recréer. Il n’existe aucun utilitaire de récupération de profil, de déplacement de profils d’un ordinateur à un autre, de sauvegarde hors ligne ou de restauration individuelle ou globale à partir de copies de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation du service de message](message-service-implementation.md)

