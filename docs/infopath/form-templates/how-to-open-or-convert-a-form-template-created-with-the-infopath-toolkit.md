---
title: Ouvrir ou convertir un modèle de formulaire créé à l’Shared Computer Toolkit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Si vous avez créé un modèle de formulaire InfoPath 2003 avec code managé au moyen de l'un des kits de ressources InfoPath 2003 pour Visual Studio, pour assurer la compatibilité avec InfoPath 2003, vous pouvez continuer à travailler sur ce modèle de formulaire et poursuivre son développement en l'ouvrant dans Microsoft InfoPath ou Visual Studio 2012.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428584"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Ouvrir ou convertir un modèle de formulaire créé à l’Shared Computer Toolkit

Si vous avez créé un modèle de formulaire InfoPath 2003 avec code managé au moyen de l'un des kits de ressources InfoPath 2003 pour Visual Studio, pour assurer la compatibilité avec InfoPath 2003, vous pouvez continuer à travailler sur ce modèle de formulaire et poursuivre son développement en l'ouvrant dans Microsoft InfoPath ou Visual Studio 2012.
  
Vous pouvez également migrer et mettre à niveau le code dans votre projet InfoPath 2003 pour utiliser le nouveau modèle objet .NET fourni par [Microsoft.Office. Espace de noms InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Dans ce cas, tout votre code doit être réécrit pour utiliser les membres de **Microsoft.Office.** Espace de noms InfoPath, mais tout le code de votre projet précédent est conservé et entouré d’instructions **#if InfoPathManagedObjectModel** et **#endif** **(C#) ou #If InfoPathManagedObject Model** et #End **If** (Visual Basic) pour votre référence. 
  
Les procédures suivantes décrivent comment ouvrir un modèle de formulaire avec code géré créé à l’aide de l’Shared Computer Toolkit InfoPath et maintenir la compatibilité avec InfoPath 2003 ou migrer et mettre à niveau vers le nouveau modèle objet InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Ouvrir un modèle de formulaire avec code managé créé au moyen du kit de ressources InfoPath et conserver la compatibilité avec InfoPath 2003 au moyen de Visual Studio Tools for Applications

1. Ouvrez le Concepteur InfoPath, puis cliquez sur **Ouvrir** sous **l’onglet** Fichier. 
    
2. Dans la boîte de dialogue Ouvrir en **mode Création,** accédez au dossier du projet dans lequel le projet Shared Computer Toolkit modèle de formulaire InfoPath est enregistré. 
    
    Par défaut, il s’agit d’un dossier dans le nom `C:\Users\`  `\Documents\Visual Studio Projects` d’utilisateur sur l’ordinateur sur lequel le projet a été créé.   Vous pouvez également déplacer le dossier vers l’emplacement où infoPath stocke Visual Studio projets 2012, qui est par défaut le nom `C:\Users\` *d’utilisateur.*  `\Documents\InfoPath Projects`
    
3. Cliquez sur le fichier nommé manifest.xsf, puis cliquez sur **Ouvrir.**
    
4. Sous l’onglet **Développeur**, cliquez sur **Éditeur de code**.
    
5. Le message suivant apparaît : « Vous devez enregistrer ce modèle de formulaire avant d'y ajouter du code Visual Basic ou C#. ». Cliquez sur **OK** pour continuer. 
    
6. Naviguez vers l'emplacement où vous voulez enregistrer le fichier, donnez un nom à celui-ci, puis cliquez sur **Enregistrer**.
    
7. Le message suivant apparaît : « Ce code a été créé avec un kit de ressources Microsoft Office InfoPath 2003 pour Microsoft Visual Studio. InfoPath doit migrer le projet de kit de ressources vers un nouveau format. ». Cliquez sur **OK** pour continuer. 
    
8. Sélectionnez le Visual Studio solution (.sln) pour le projet, puis cliquez sur **Ouvrir.**
    
9. Le message suivant apparaît : « La migration de votre projet est terminée ». Cliquez sur **OK** pour continuer. 
    
10. Le message « Le code de ce formulaire utilise le modèle objet InfoPath 2003 » s’affiche avec l’invite « Voulez-vous mettre à niveau votre code pour utiliser le modèle objet InfoPath Microsoft Office ? » Cliquez **sur Non** pour conserver la compatibilité avec InfoPath 2003 et continuer à travailler avec le modèle objet fourni par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
    
    Pour plus d’informations sur l’utilisation de modèles de formulaires avec code géré compatibles avec InfoPath 2003, voir [Developing Form Templates Using the InfoPath 2003 Object Model](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Ouvrir un modèle de formulaire avec code managé créé au moyen du kit de ressources InfoPath et le mettre à niveau pour qu’il utilise le nouveau modèle objet InfoPath au moyen de Visual Studio Tools for Applications

1. Ouvrez le Concepteur InfoPath, puis cliquez sur **Ouvrir** sous **l’onglet** Fichier. 
    
2. Sous **Ouvrir un modèle de formulaire**, cliquez sur **Sur mon ordinateur**.
    
3. Dans la boîte de dialogue Ouvrir en **mode Création,** accédez au dossier du projet dans lequel le projet Shared Computer Toolkit modèle de formulaire InfoPath est enregistré. 
    
    Par défaut, il s’agit d’un dossier dans le nom `C:\Users\` *d’utilisateur* `\Documents\Visual Studio Projects` sur l’ordinateur sur lequel le projet a été créé.   Vous pouvez également déplacer le dossier vers l’emplacement où infoPath stocke Visual Studio projets 2012, qui est par défaut le nom `C:\Users\` *d’utilisateur.*  `\Documents\InfoPath Projects`
    
4. Cliquez sur le fichier nommé manifest.xsf, puis cliquez sur **Ouvrir.**
    
5. Sous l’onglet **Développeur**, cliquez sur **Éditeur de code**.
    
6. Le message suivant apparaît : « Vous devez enregistrer ce modèle de formulaire avant d'y ajouter du code Visual Basic ou C#. ». Cliquez sur **OK** pour continuer. 
    
7. Naviguez vers l'emplacement où vous voulez enregistrer le fichier, donnez un nom à celui-ci, puis cliquez sur **Enregistrer**.
    
8. Le message suivant apparaît : « Ce code a été créé avec un kit de ressources Microsoft Office InfoPath 2003 pour Microsoft Visual Studio. InfoPath doit migrer le projet de kit de ressources vers un nouveau format. ». Cliquez sur **OK** pour continuer. 
    
9. Sélectionnez le Visual Studio solution (.sln) pour le projet, puis cliquez sur **Ouvrir.**
    
10. Le message suivant apparaît : « La migration de votre projet est terminée ». Cliquez sur **OK** pour continuer. 
    
11. Le message « Le code de ce formulaire utilise le modèle objet InfoPath 2003 » s’affiche avec l’invite « Voulez-vous mettre à niveau votre code pour utiliser le modèle objet InfoPath Microsoft Office ? » Cliquez **sur Oui** pour mettre à niveau le modèle de formulaire afin d’utiliser le nouveau modèle objet avec code géré fourni par [Microsoft.Office. Espace de noms InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
    
    Votre code de formulaire est ouvert dans l’éditeur de code Visual Studio 2012 avec tout le code de votre projet précédent entouré d’instructions **#if** **InfoPathManagedObjectModel** et **#endif** (C#) ou **#If InfoPathManagedObjectModel** et **#End If** (Visual Basic) pour votre référence. L’ensemble de ce code devra être réécrit pour utiliser des membres du modèle objet fourni par l’espace de noms **Microsoft.Office.InfoPath**. 
    
    Pour plus d’informations sur l’utilisation des modèles de formulaire avec code géré qui utilisent le nouveau modèle objet InfoPath avec code géré, voir Développement de modèles de formulaire [InfoPath avec code.](developing-infopath-form-templates-with-code.md)
    

