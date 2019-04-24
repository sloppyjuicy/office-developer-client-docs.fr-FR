---
title: Prise en charge de l'installation du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350630"
---
# <a name="supporting-message-service-installation"></a>Prise en charge de l'installation du service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le programme d'installation pour l'installation de votre service de messagerie doit effectuer les opérations suivantes:
  
1. Copiez les fichiers de service de messagerie, tels que les dll du service de messagerie et du fournisseur de services, à partir d'un CD-ROM ou d'un disque, vers un lecteur local de la station de travail. Les fichiers qui doivent être copiés dépendent de votre service de messagerie. En règle générale, vous copiez au moins une DLL.
    
2. Ajoutez des entrées au fichier de configuration MAPISVC. inf. Pour plus d'informations sur la façon de modifier ce fichier afin de prendre en charge les fournisseurs de services dans votre service de messagerie, consultez la rubrique [file format of MapiSvc. inf](file-format-of-mapisvc-inf.md).
    
3. Ajoutez des entrées, selon le cas, dans le registre système pour les services de messagerie. Pour plus d'informations sur la façon dont les entrées doivent apparaître dans le registre système, consultez [la rubrique Installation du sous-système MAPI](installing-the-mapi-subsystem.md).
    
4. Créez un profil par défaut s'il n'existe pas encore de l'un des éléments suivants:
    
  - L'Assistant Profil pour créer un profil à l'aide de l'intervention de l'utilisateur via une série de boîtes de dialogue. Pour plus d'informations sur l'utilisation de l'Assistant Profil, consultez la rubrique [création d'un profil à l'aide de l'Assistant Profil](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Le panneau de configuration pour créer un profil à l'aide de l'interaction utilisateur. Le panneau de configuration offre davantage de flexibilité à l'utilisateur que l'Assistant Profil pour la configuration des services de message et la définition des propriétés de profil. 
    
Placez le programme d'installation dans un répertoire public désigné. Ceci est important, car la plupart des clients de configuration, tels que le panneau de configuration, exigent que les utilisateurs entrent le nom du répertoire. Le panneau de configuration appelle un programme d'installation lorsqu'un utilisateur clique sur le bouton **Ajouter** , appelle la boîte de dialogue **disquette** et spécifie le chemin d'accès au programme. Le panneau de configuration exécute le programme et appelle la fonction de point d'entrée de votre service de messagerie avec le paramètre _ulContext_ défini sur MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Étant donné que les profils sont une partie intégrante de l'architecture MAPI, assurez-vous que votre programme d'installation ne stocke rien dans le profil par défaut qui serait difficile à recréer. Il n'existe pas d'utilitaires pour la récupération de profil, pour le transfert des profils d'un ordinateur à un autre, pour une sauvegarde hors ligne ou pour une restauration individuelle ou globale à partir de copies de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation du service de messagerie](message-service-implementation.md)

