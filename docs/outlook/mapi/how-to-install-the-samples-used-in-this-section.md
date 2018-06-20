---
title: Installer les exemples de cette section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4c5b6cbdda63dcb79b23253e0db695ae658c4fa4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783489"
---
# <a name="install-the-samples-used-in-this-section"></a>Installer les exemples de cette section

**S’applique à**: Outlook 
  
Pour installer l’application MFCMAPI et projet CreateOutlookItemsAddin pour afficher et exécuter l’exemple de code référencée par les rubriques de la section [Création des éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) , procédez comme suit. 

Pour télécharger et installer les exemples utilisés dans la « utilisation de MAPI pour créer des éléments Outlook » section, procédez comme suit.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Pour télécharger et installer l’application MFCMAPI et ouvrez le projet CreateOutlookItemsAddin

1. Téléchargez la version actuelle de [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) exécutable dans un dossier sur votre système. 
    
2. Extraire le fichier MFCMapi.exe MFCMapi.exe. _version_.zip dans un dossier vide sur votre disque dur.
    
3. Téléchargez la version actuelle du projet [CreateOutlookItemsAddin](http://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. Extraire tous les fichiers dans le fichier CreateOutlookItemsAddin.zip dans le dossier où vous avez extrait le fichier MFCMapi.exe à l’étape 2.
    
5. Copiez MFCMapi.exe à partir du dossier utilisé à l’étape 2 pour le répertoire de build pour le projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Ouvrez le projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) dans Visual Studio pour examiner le code source. Reportez-vous aux rubriques de la section [Création des éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) pour déterminer les fichiers source à ouvrir. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Exécutez MFCMAPI et le projet CreateOutlookItemsAddin

Les étapes suivantes supposent que vous avez téléchargé et installé la version actuelle de l’exécutable MFCMAPI et le projet CreateOutlookItemsAddin comme décrit dans la procédure précédente. Ces étapes vous guide pour les éléments de menu **compléments** qui vous permettent de créer des éléments Outlook à l’aide de l’application de MFCMAPI et le projet CreateOutlookItemsAddin. 
  
> [!NOTE]
> Le dossier sélectionné à l’étape 8 et la commande sélectionnée à l’étape 9, varie selon le type d’élément présentée dans une des rubriques de la section [Création des éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Pour exécuter l’application MFCMAPI et les commandes de menu Compléments

1. Démarrez Mfcmapi.exe dans le dossier CreateOutlookItemsAddin\Debug qui est créé lorsque vous suivez les instructions d’installation.
    
2. Cliquez sur **OK** pour fermer l’écran de démarrage MFCMAPI. 
    
3. Dans le menu **Session** , cliquez sur **ouverture de session et affichage de la Table magasin**.
    
4. Dans la boîte de dialogue **Choix d’un profil** , sélectionnez le profil approprié, puis cliquez sur **OK**. 
    
5. Double-cliquez sur **boîte aux lettres - _[Nom utilisateur]_ ** dans la liste table banque. 
    
6. Dans l’arborescence de dossiers, développez le nœud racine. Le nom affiché pour le nœud racine varie selon le type de profil sélectionné. Ce nœud s’affiche généralement sous **racine - boîte aux lettres**.
    
7. Dans l’arborescence de dossiers, développez le nœud qui contient la banque d’informations. Le nom affiché pour ce nœud varie selon le type de profil sélectionné. Ce nœud s’affiche généralement sous **IPM_SUBTREE** ou **En haut de la banque d’informations**.
    
8. Double-cliquez sur le dossier pour le type d’élément à créer. Par exemple, pour créer un rendez-vous, cliquez sur le dossier de **rendez-vous** . 
    
9. Dans le menu **compléments** , cliquez sur la commande appropriée pour l’élément à créer. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Télécharger et afficher le code de l’application de MFCMAPI

Certaines rubriques font référence au code source à partir de l’application MFCMAPI proprement dite. Les étapes suivantes décrivent comment télécharger le code source MFCMAPI et l’afficher dans Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Pour télécharger et afficher le code source d’application MFCMAPI

1. Télécharger le code source pour la version actuelle de l’application [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) dans un dossier sur votre système. 
    
2. Extrayez les fichiers dans MFCMAPI - .zip _l’ensemble de modifications_dans un dossier vide sur votre disque dur.
    
3. Ouvrez le projet MFCMapi (\ _foldername_\ MFCMapi.vcproj) dans Visual Studio pour examiner le code source.
    
## <a name="see-also"></a>Voir aussi

- [Créer un élément de courrier Simple](how-to-create-a-simple-mail-item.md)
- [Créer une tâche périodique Simple](how-to-create-a-simple-recurrent-task-item.md)
- [Créer un rendez-vous périodique complexes](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lire et analyser une périodicité](how-to-read-and-parse-a-recurrence-pattern.md)

