---
title: Installation des exemples utilisés dans cette section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345548"
---
# <a name="install-the-samples-used-in-this-section"></a>Installation des exemples utilisés dans cette section

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour installer l'application MFCMAPI et le projet CreateOutlookItemsAddin pour afficher et exécuter l'exemple de code référencé par les rubriques de la section [création d'éléments Outlook à l'aide de MAPI](creating-outlook-items-by-using-mapi.md) , procédez comme suit. 

Pour télécharger et installer les exemples utilisés dans la section «utilisation de MAPI pour créer des éléments Outlook», procédez comme suit.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Pour télécharger et installer l'application MFCMAPI et ouvrir le projet CreateOutlookItemsAddin

1. Téléchargez la version actuelle du fichier exécutable [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) vers un dossier sur votre système. 
    
2. ExTrayez le fichier MFCMapi. exe dans MFCMapi. exe. _version_. zip dans un dossier vide de votre disque dur.
    
3. Téléchargez la version actuelle du projet [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. ExTrayez tous les fichiers du fichier CreateOutlookItemsAddin. zip dans le dossier où vous avez extrait le fichier MFCMapi. exe à l'étape 2.
    
5. Copiez MFCMapi. exe à partir du dossier utilisé à l'étape 2 dans le répertoire de création pour le projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Ouvrez le projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) dans Visual Studio pour examiner le code source. RePortez-vous aux rubriques de la section [création d'éléments Outlook à l'aide de MAPI](creating-outlook-items-by-using-mapi.md) pour déterminer les fichiers sources à ouvrir. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Exécuter MFCMAPI et le projet CreateOutlookItemsAddin

Les étapes suivantes supposent que vous avez téléchargé et installé la version actuelle du fichier exécutable MFCMAPI et le projet CreateOutlookItemsAddin, comme décrit dans la procédure précédente. Ces étapes vous guident dans les **** éléments de menu AddIns qui vous permettent de créer des éléments Outlook à l'aide de l'application MFCMAPI et du projet CreateOutlookItemsAddin. 
  
> [!NOTE]
> Le dossier que vous sélectionnez à l'étape 8, et la commande sélectionnée à l'étape 9, dépendent du type d'élément décrit dans l'une des rubriques de la section [création d'éléments Outlook à l'aide de MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Pour exécuter les commandes du menu application et AddIns MFCMAPI

1. Démarrez MFCMAPI. exe dans le dossier CreateOutlookItemsAddin\Debug créé lorsque vous suivez les instructions d'installation.
    
2. Cliquez sur **OK** pour fermer l'écran de démarrage MFCMAPI. 
    
3. Dans le menu **session** , cliquez sur **ouverture de session et afficher la table de magasin**.
    
4. Dans la boîte de dialogue **choisir un profil** , sélectionnez le profil correct, puis cliquez sur **OK**. 
    
5. Double-cliquez sur **boîte aux lettres- _[nom d'utilisateur]_ ** dans l'affichage liste des tables du Store. 
    
6. Dans l'arborescence des dossiers, développez le nœud racine. Le nom affiché pour le nœud racine varie en fonction du type de profil sélectionné. En règle générale, ce nœud est affiché sous la forme d' **une boîte aux lettres racine**.
    
7. Dans l'arborescence des dossiers, développez le nœud qui contient la Banque d'informations. Le nom affiché pour ce nœud varie en fonction du type de profil sélectionné. En règle générale, ce nœud est affiché sous la forme **IPM_Subtree** ou en **haut de la Banque d'informations**.
    
8. Double-cliquez sur le dossier du type d'élément à créer. Par exemple, pour créer un rendez-vous, cliquez sur le dossier rendez- **vous** . 
    
9. Dans le **** menu AddIns, cliquez sur la commande appropriée pour l'élément à créer. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Téléchargement et affichage de code à partir de l'application MFCMAPI

Certaines rubriques font référence au code source de l'application MFCMAPI elle-même. Les étapes suivantes décrivent comment télécharger le code source MFCMAPI et l'afficher dans Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Pour télécharger et afficher le code source de l'application MFCMAPI

1. Téléchargez le code source de la version actuelle de l'application [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) dans un dossier sur votre système. 
    
2. ExTrayez les fichiers dans MFCMAPI- _ChangeSet_. zip dans un dossier vide sur votre disque dur.
    
3. Ouvrez le projet MFCMapi (\ _nom_dossier_\ MFCMapi. vcproj) dans Visual Studio pour examiner le code source.
    
## <a name="see-also"></a>Voir aussi

- [Créer un élément de courrier simple](how-to-create-a-simple-mail-item.md)
- [Créer un élément de tâche récurrente simple](how-to-create-a-simple-recurrent-task-item.md)
- [Créer un élément de rendez-vous récurrent complexe](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lire et analyser une périodicité](how-to-read-and-parse-a-recurrence-pattern.md)

