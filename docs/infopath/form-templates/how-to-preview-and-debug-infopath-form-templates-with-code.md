---
title: Afficher un aperçu et déboguer les modèles de formulaire InfoPath avec Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath avec Visual Studio 2012 permet le débogage en exécutant le code du formulaire en mode Aperçu. Lorsque vous commencez à déboguer le code du formulaire, votre projet est compilé et InfoPath affiche votre formulaire dans la fenêtre d'aperçu InfoPath. Lors du passage sur une ligne de code contenant un point d'arrêt, le focus passe dans l'Éditeur de code. Si vous continuez au-delà d'un point d'arrêt, le focus repasse dans la fenêtre d'aperçu. Le débogage s'arrête lorsque vous fermez la fenêtre d'aperçu.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782363"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Afficher un aperçu et déboguer les modèles de formulaire InfoPath avec Code

Microsoft InfoPath avec Visual Studio 2012 permet le débogage en exécutant le code du formulaire en mode Aperçu. Lorsque vous commencez à déboguer le code du formulaire, votre projet est compilé et InfoPath affiche votre formulaire dans la fenêtre d'aperçu InfoPath. Lors du passage sur une ligne de code contenant un point d'arrêt, le focus passe dans l'Éditeur de code. Si vous continuez au-delà d'un point d'arrêt, le focus repasse dans la fenêtre d'aperçu. Le débogage s'arrête lorsque vous fermez la fenêtre d'aperçu.
  
Vous pouvez également modifier les options de formulaire du modèle de formulaire dont vous souhaitez afficher un aperçu et que vous voulez déboguer en utilisant un rôle utilisateur spécifique, un fichier de données exemple ou en spécifiant le domaine dans lequel le formulaire sera publié. 
  
> [!NOTE]
> [!REMARQUE] Il n'est pas possible de déboguer les modèles de formulaires après leur déploiement au moment de l'exécution à partir des Visual Studio 2012. Cela comprend les modèles de formulaires qui sont compatibles uniquement avec InfoPath, ainsi que ceux qui sont compatibles avec InfoPath et le navigateur Web utilisant InfoPath Forms Services. Cependant, vous pouvez enregistrer des valeurs dans un champ à partir du code à l'exécution pour vous aider à résoudre les problèmes de la logique métier d'un modèle de formulaire. Pour plus d’informations sur la procédure à suivre, voir le [Journal des valeurs à un champ pour le débogage](how-to-log-values-to-a-field-for-debugging.md). 
  
## <a name="debugging-in-preview-mode"></a>Débogage en mode Aperçu

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>Pour déboguer un projet InfoPath en mode Aperçu

1. Créez ou ouvrez un modèle de formulaire InfoPath avec code managé dans Visual Studio 2012.
    
2. Définissez un ou plusieurs points d'arrêt dans votre code de formulaire dans l'éditeur de code en cliquant sur la barre grise à gauche de la ligne de code où vous voulez insérer un point d'arrêt.
    
    Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution marquera une pause à ce point d'arrêt dans votre code de formulaire.
    
3. Dans le menu **Débogage**, cliquez sur **Démarrer le débogage**; ou appuyez sur F5.
    
    Le projet est compilé et le formulaire s'affiche dans la fenêtre d'aperçu.
    
4. Utilisez le formulaire jusqu'à ce que vous rencontriez une ligne contenant un point d'arrêt.
    
    Le focus revient dans l'éditeur de code.
    
5. Dans le menu **Débogage**, cliquez sur **Continuer** ou appuyez sur F5.
    
6. Lorsque vous avez terminé le débogage, fermez la fenêtre d'aperçu ou, dans le menu **Débogage**, cliquez sur **Arrêter le débogage**.
    
> [!NOTE]
> Pour déboguer un modèle de formulaire InfoPath avec code managé lors de l’utilisation d’un membre de modèle objet nécessitant une confiance totale, vous devez configurer votre modèle de formulaire, comme indiqué dans [l’Aperçu et déboguer les modèles de formulaires qui nécessitent une autorisation totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  
## <a name="using-a-sample-data-file"></a>Utilisation d'un fichier exemple de données

Par défaut, le débogage et l'aperçu utilisent le fichier template.xml créé lors de la création d'un modèle de formulaire. Vous pouvez créer votre propre fichier de données et en spécifier l'utilisation lors de l'aperçu ou du débogage en suivant l'une des procédures ci-dessous. 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>Pour spécifier un fichier exemple de données à utiliser pour le débogage ou l'aperçu dans Visual Studio Tools for Applications

1. Pour afficher template.xml, ouvrez le modèle de formulaire en mode Création dans InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, cliquez sur **Enregistrement**, sur **Enregistrer le modèle de formulaire sous**, puis cliquez sur **Fichiers source**.
    
3. Enregistrez les fichiers du modèle de formulaire dans un dossier, puis ouvrez le fichier template.xml dans un éditeur de texte.
    
4. Créez et enregistrez un fichier avec la même structure que template.xml avec les données exemple que vous voulez utiliser.
    
5. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**. 
    
6. Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis sous **Exemple de données** spécifiez le fichier exemple que vous avez créé dans la zone **Emplacement du fichier**. 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Spécification d'un rôle d'utilisateur à utiliser lors du débogage ou de l'affichage de l'aperçu

Si le formulaire dans lequel vous travaillez contient des rôles d'utilisateur, vous pouvez spécifier le rôle d'utilisateur à utiliser lors du débogage ou de l'aperçu du formulaire. Pour plus d'informations sur la définition des rôles d'utilisateur, recherchez « Rôle d'utilisateur » dans l'aide d'InfoPath.
  
> [!NOTE]
> [!REMARQUE] L'option permettant de spécifier un rôle d'utilisateur n'est pas disponible si la compatibilité de votre modèle de formulaire est paramétrée comme **Formulaires de navigateur Web**. Les rôles des utilisateurs ne sont pas pris en charge dans les modèles de formulaires ouverts dans le navigateur à partir d'InfoPath Forms Services. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>Pour spécifier un rôle à utiliser pour le débogage ou l'aperçu

1. Si vous travaillez dans Visual Studio 2012, basculez vers le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**. 
    
3. Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis spécifiez le rôle d'utilisateur à utiliser dans la zone de liste déroulante **Aperçu en tant que**. 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Spécification d'un domaine à utiliser lors du débogage ou de l'affichage de l'aperçu

Vous pouvez afficher un aperçu d'un formulaire comme s'il avait été publié dans un domaine spécifique. Ce paramètre fonctionne uniquement si le niveau de sécurité du modèle de formulaire est explicitement défini sur **Domaine**.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>Pour spécifier un domaine à utiliser pour le débogage ou l'aperçu

1. Si vous travaillez dans Visual Studio 2012, basculez vers le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**. 
    
3. Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis spécifiez le domaine à utiliser lors de l'aperçu ou du débogage dans la zone **Domaine**. 
    
4. Cliquez sur la catégorie **Sécurité et approbation** de la boîte de dialogue **Options de formulaire**, désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**, puis cliquez sur **Domaine**.
    

