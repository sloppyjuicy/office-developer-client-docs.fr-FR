---
title: Configurer les paramètres de sécurité pour les modèles de formulaire avec du code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
ms.localizationpriority: medium
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Vous pouvez personnaliser le jeu d'autorisations qui est appliqué à un modèle de formulaire InfoPath avec code managé en utilisant le composant logiciel enfichable Configuration .NET.
ms.openlocfilehash: da0ac6116c2e3ad0a87f5d7a2fc3e8c30872d64d
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893689"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Configurer les paramètres de sécurité pour les modèles de formulaire avec du code

Vous pouvez personnaliser le jeu d'autorisations qui est appliqué à un modèle de formulaire InfoPath avec code managé en utilisant le composant logiciel enfichable Configuration .NET.
  
Le CLR (Common Language Runtime) hébergé par InfoPath recherche un groupe de codes prédéfini nommé *Modèles de formulaire InfoPath* au niveau de la stratégie machine sous le groupe All_Code. Le CLR applique les jeux d'autorisations définis dans ce groupe au domaine d'application (AppDomain) dans lequel le formulaire s'exécute. Ceci vous permet de personnaliser les jeux d'autorisations qui sont accordés aux modèles de formulaire de code managé InfoPath. Par exemple, vous pouvez accorder à un modèle de formulaire téléchargé depuis `https://MySite` l'autorisation d'accès à Active Directory.
  
Pour que la stratégie de sécurité personnalisée définie à l'aide du composant logiciel enfichable Configuration .NET soit appliquée, elle doit être déployée sur tous les ordinateurs clients sur lesquels le modèle de formulaire sera exécuté.
  
Pour plus d’informations sur le modèle de sécurité pour les modèles de formulaires de code managé InfoPath, consultez [À propos du modèle de sécurité pour les modèles de formulaire avec code](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Création d'un groupe de codes pour les modèles de formulaire InfoPath

La procédure suivante crée un groupe de codes qui n’accorde aucune autorisation aux modèles de formulaires de code managé InfoPath (à l’exception de ceux qui sont installés ou inscrits sur votre ordinateur local) sous lequel vous pouvez attribuer des jeux d’autorisations à des modèles de formulaire InfoPath situés dans des URL ou des UNCs spécifiques. Pour plus d’informations sur la création et l’affectation de jeux d’autorisations à des groupes de code au sein du `InfoPath Form Templates` groupe de codes, consultez la procédure suivante.
  
> [!NOTE]
> [!REMARQUE] Contrairement à l'outil **Configuration Microsoft .NET Framework 1.1** qui est installé avec Microsoft .NET Framework 1.1 Redistributable Package, **Configuration Microsoft .NET Framework 2.0** est uniquement installé avec le Kit de développement logiciel (SDK) Microsoft .NET Framework 2.0.
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>Pour créer un groupe de codes de sécurité personnalisé pour les formulaires InfoPath avec code managé

1. Dans le menu **Démarrer**, pointez sur **Outils d'administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.

    Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2,0**.

2. Dans **Poste de travail**, développez les nœuds **Stratégie de sécurité du runtime**, **Ordinateur**, **Groupes de codes** et **All_Code**, puis cliquez avec le bouton droit sur le nœud **All_Code** et cliquez sur **Nouveau** pour ouvrir la boîte de dialogue **Créer un groupe de codes**.

3. Attribuez un nom au nouveau groupe de codes  `InfoPath Form Templates` (ce texte doit être exact), puis cliquez sur **Suivant**.

4. Définissez le type de condition du groupe de codes sur **Tout le code**, puis cliquez sur **Suivant**.

5. Cliquez sur **Utiliser un jeu d'autorisations existant**, affectez le jeu d'autorisations **Nothing** au groupe de codes, cliquez sur **Suivant**, puis sur **Terminer**.

6. Pour appliquer les nouveaux paramètres, fermez puis redémarrez InfoPath.

Si vous le souhaitez, vous pouvez gérer le jeu d'autorisations pour tous les modèles de formulaire InfoPath avec code managé en attribuant un jeu d'autorisations autre que **Rien** au groupe de codes **Modèles de formulaire InfoPath**.
> [!NOTE]
> Vous pouvez modifier à tout moment le jeu d'autorisations d'un groupe de codes de sécurité en cliquant avec le bouton droit sur le groupe dans le composant **Configuration .NET 2,0**, puis en cliquant sur **Propriétés**, puis sur l'onglet **Jeu d'autorisations**.
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Affectation d'une autorisation totale à des formulaires comportant une URL ou une UNC spécifique

Vous pouvez créer des groupes de codes sous le groupe **Modèles de formulaires InfoPath** pour accorder une autorisation totale à des modèles de formulaires provenant d’une URL ou d’un emplacement UNC spécifique. Ainsi, tous les modèles de formulaires publiés à l’emplacement spécifié s’exécuteront avec une autorisation totale.
  
> [!NOTE]
> [!REMARQUE] Un modèle de formulaire chargé depuis l'ordinateur local (groupe de codes de la zone MyComputer) est chargé par InfoPath à l'aide d'une URL aléatoire. De ce fait, vous ne pouvez pas utiliser la procédure qui suit pour accorder le jeu d'autorisations Autorisation totale à un tel modèle de formulaire. Pour accorder à un modèle de formulaire installé localement le jeu d’autorisations FullTrust, utilisez l’une des procédures décrites dans la section « Déploiement de modèles de formulaire qui nécessitent une confiance totale » de la rubrique [Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md) .
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>Pour affecter une autorisation totale aux formulaires InfoPath situés à un emplacement URL ou UNC spécifique

1. Dans le menu **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.

    Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2.0**.

2. Dans **Poste de travail**, développez les nœuds **Stratégie de sécurité du runtime**, **Ordinateur**, **Groupes de code**, **All_Code**, puis cliquez sur le nœud **Modèles de formulaires InfoPath**.

3. Dans la liste **Tâches** du volet de droite, cliquez sur **Ajouter un groupe de codes enfants**, donnez un nom à ce groupe de codes, puis cliquez sur **Suivant**.

4. Dans la liste **Type de condition pour ce groupe de codes**, sélectionnez **URL**, puis entrez l'URL ou l'UNC de l'emplacement des modèles de formulaires InfoPath avec code managé auxquels vous souhaitez accorder le jeu d'autorisations **Autorisation totale**.

    Pour restreindre le jeu d'autorisations à un seul modèle de formulaire, spécifiez le chemin complet de ce modèle de formulaire. Par exemple :

     `\\MyServer\MyShare\MyFormTemplate.xsn`

     `https://MySite/MySubsite/MyFormTempate.xsn`

    Pour accorder un jeu d'autorisations à tous les modèles de formulaires d'une URL ou d'une UNC, n'indiquez pas le nom du modèle et ajoutez un astérisque à la fin de l'URL ou de l'UNC. Par exemple :

     `\\MyServer\MyShare\*`

     `https://MySite/MySubsite/*`

5. Cliquez sur **Suivant**, puis sur **Utiliser un jeu d'autorisations existant** et attribuez le jeu d'autorisations **Autorisation totale** au groupe de codes.

6. Cliquez sur **Suivant**, puis sur **Terminer**.

7. Pour appliquer les nouveaux paramètres, fermez puis redémarrez InfoPath.

> [!NOTE]
> [!REMARQUE] Pour appliquer un jeu d'autorisations plus restrictif ou personnalisé, sélectionnez l'option appropriée à la place de **Autorisation totale** à l'étape 4.
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Création d'un package de déploiement pour la stratégie de sécurité d'InfoPath

Après avoir défini une stratégie de sécurité personnalisée pour les modèles de formulaires InfoPath avec code managé, vous pouvez créer un package Windows Installer (.msi) pour déployer la stratégie de sécurité sur les ordinateurs des utilisateurs à l'aide de la Stratégie de groupe ou de Microsoft Systems Management Server.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>Pour créer un package de déploiement pour la stratégie de sécurité personnalisée d’InfoPath

1. Dans le menu **Démarrer**, pointez sur **Outils d'administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.

    Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2.0**.

2. Cliquez avec le bouton droit sur **Stratégie de sécurité du runtime**, puis cliquez sur **Créer un package de déploiement**.

3. Sous **Sélectionnez le niveau de stratégie de sécurité à déployer**, cliquez sur **Ordinateur**, spécifiez le dossier et le nom de fichier du package Windows Installer Package, puis cliquez sur **Suivant**.

4. Cliquez sur **Terminer** pour créer le package de déploiement.

5. Pour plus d’informations sur l’utilisation de l’outil de configuration .NET Framework, recherchez « .NET Framework Configuration Tool (Mscorcfg.msc) » sur le site web MSDN ou l’aide de Visual Studio.

## <a name="see-also"></a>Voir aussi

[À propos du modèle de sécurité pour les modèles de formulaire avec code](about-the-security-model-for-form-templates-with-code.md)
