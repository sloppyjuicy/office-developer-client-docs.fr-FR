---
title: Installation des exemples utilisés dans cette section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
ms.openlocfilehash: 30221c39cad7bd18a83e3f5ab527884e3808d12a
ms.sourcegitcommit: 96361960306aae696ed3f7a9f07df7c9dca7f2cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2022
ms.locfileid: "68689876"
---
# <a name="install-the-samples-used-in-this-section"></a>Installation des exemples utilisés dans cette section

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour installer l’application MFCMAPI et le projet CreateOutlookItemsAddin afin d’afficher et d’exécuter l’exemple de code référencé par les rubriques de la section [Création d’éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) , procédez comme suit. 

Pour télécharger et installer les exemples utilisés dans la section « Utilisation de MAPI pour créer des éléments Outlook », procédez comme suit.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Pour télécharger et installer l’application MFCMAPI et ouvrir le projet CreateOutlookItemsAddin

1. Téléchargez la version actuelle de l’exécutable [MFCMAPI](https://aka.ms/mfcmapi) dans un dossier sur votre système. 
    
2. Extrayez le fichier MFCMapi.exe dans MFCMapi.exe. _version_.zip à un dossier vide sur votre disque dur.
    
3. Téléchargez la version actuelle du projet [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. Extrayez tous les fichiers du fichier CreateOutlookItemsAddin.zip dans le dossier où vous avez extrait le fichier MFCMapi.exe à l’étape 2.
    
5. Copiez MFCMapi.exe du dossier utilisé à l’étape 2 dans le répertoire de build du projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Ouvrez le projet CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) dans Visual Studio pour examiner le code source. Reportez-vous aux rubriques de la section [Création d’éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) pour déterminer les fichiers sources à ouvrir. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Exécuter MFCMAPI et le projet CreateOutlookItemsAddin

Les étapes suivantes supposent que vous avez téléchargé et installé la version actuelle de l’exécutable MFCMAPI et le projet CreateOutlookItemsAddin, comme décrit dans la procédure précédente. Ces étapes vous guident vers les éléments de menu **Addins** qui vous permettent de créer des éléments Outlook à l’aide de l’application MFCMAPI et du projet CreateOutlookItemsAddin. 
  
> [!NOTE]
> Le dossier que vous sélectionnez à l’étape 8 et la commande que vous sélectionnez à l’étape 9 dépendent du type d’élément abordé dans l’une des rubriques de la section [Création d’éléments Outlook à l’aide de MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Pour exécuter l’application MFCMAPI et les commandes de menu Addins

1. Démarrez Mfcmapi.exe dans le dossier CreateOutlookItemsAddin\Debug créé lorsque vous suivez les instructions d’installation.
    
2. Cliquez sur **OK** pour ignorer l’écran de démarrage MFCMAPI. 
    
3. Dans le menu **Session** , cliquez sur **Ouverture de session et Afficher la table du Magasin**.
    
4. Dans la boîte de dialogue **Choisir un profil** , sélectionnez le profil approprié, puis cliquez sur **OK**. 
    
5. Double-cliquez sur **Boîte aux lettres  _- [Nom d’utilisateur]_** dans l’affichage liste des tables du magasin. 
    
6. Dans l’arborescence des dossiers, développez le nœud racine. Le nom affiché pour le nœud racine varie en fonction du type de profil sélectionné. En règle générale, ce nœud est affiché sous **la forme Racine - Boîte aux lettres**.
    
7. Dans l’arborescence des dossiers, développez le nœud qui contient la banque d’informations. Le nom affiché pour ce nœud varie en fonction du type de profil sélectionné. En règle générale, ce nœud est affiché en tant que **IPM_SUBTREE** ou **En haut de la banque d’informations**.
    
8. Double-cliquez sur le dossier du type d’élément à créer. Par exemple, pour créer un rendez-vous, cliquez sur le dossier **Rendez-vous** . 
    
9. Dans le menu **Addins** , cliquez sur la commande appropriée pour l’élément à créer. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Télécharger et afficher le code à partir de l’application MFCMAPI

Certaines rubriques font référence au code source de l’application MFCMAPI elle-même. Les étapes suivantes décrivent comment télécharger le code source MFCMAPI et l’afficher dans Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Pour télécharger et afficher le code source de l’application MFCMAPI

1. Téléchargez le code source de la version actuelle de l’application [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) dans un dossier sur votre système. 
    
2. Extrayez les fichiers dans _l’ensemble de modifications_ MFCMAPI-.zip dans un dossier vide sur votre disque dur.
    
3. Ouvrez le projet MFCMapi (\ _nom_dossier_\ MFCMapi.vcproj) dans Visual Studio pour examiner le code source.
    
## <a name="see-also"></a>Voir aussi

- [Créer un élément de courrier simple](how-to-create-a-simple-mail-item.md)
- [Créer un élément de tâche récurrent simple](how-to-create-a-simple-recurrent-task-item.md)
- [Créer un élément de rendez-vous récurrent complexe](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lire et analyser un modèle de périodicité](how-to-read-and-parse-a-recurrence-pattern.md)

