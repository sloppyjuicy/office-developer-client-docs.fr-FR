---
title: Prise en charge de l’installation du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1f82741e3c44c589a18a1428fd68cebe6a501d5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581992"
---
# <a name="supporting-message-service-installation"></a>Prise en charge de l’installation du service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le programme d’installation pour l’installation de votre service de message doit effectuer les opérations suivantes :
  
1. Copiez les fichiers de service de message, telles que le service de message et le fournisseur de services de DLL, à partir d’un CD-ROM ou un disque, sur un lecteur local sur la station de travail. Les fichiers qui doivent être copiés dépendent de votre service de message. En règle générale, vous allez copier au moins une DLL.
    
2. Ajouter des entrées dans le fichier de configuration Mapisvc.inf. Pour plus d’informations sur la modification de ce fichier pour prendre en charge les fournisseurs de services dans votre service de message, voir le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Ajouter des entrées, selon le cas, dans le Registre système pour les services de messagerie. Pour plus d’informations sur la façon dont les entrées doivent apparaître dans le Registre système, consultez [installation du sous-système MAPI](installing-the-mapi-subsystem.md).
    
4. Créer un profil par défaut s’il n’existe pas encore à l’aide d’un des éléments suivants :
    
  - L’Assistant profil pour créer un profil à l’aide d’intervention de l’utilisateur à travers une série de boîtes de dialogue. Pour plus d’informations sur l’utilisation de l’Assistant profil, voir [Création d’un profil à l’aide de l’Assistant profil](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Le panneau pour créer un profil à l’aide d’intervention de l’utilisateur. Le panneau de configuration offre davantage de flexibilité que l’Assistant profil pour configurer les services de message et la définition des propriétés de profil à l’utilisateur. 
    
Placez le programme d’installation dans un répertoire public désigné. Ceci est important parce que la plupart des clients de configuration, comme le panneau de configuration, exigent que les utilisateurs entrent le nom du répertoire. Le panneau de configuration appelle un programme d’installation lorsqu’un utilisateur clique sur le bouton **Ajouter** , appelle la boîte de dialogue **Disque** et spécifie le chemin d’accès au programme. Le panneau de configuration s’exécute le programme et appelle la fonction de point d’entrée de votre service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Étant donné que les profils sont un composant de l’architecture MAPI consommables, n’oubliez pas que votre programme d’installation ne stocke pas rien dans le profil par défaut qui serait difficile à recréer. Il n’existe aucun utilitaire pour la récupération du profil, sur le déplacement des profils à partir d’un ordinateur à un autre, de sauvegarde hors connexion ou pour effectuer la restauration individuelle ou globale à partir des copies de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation du service de messagerie](message-service-implementation.md)

