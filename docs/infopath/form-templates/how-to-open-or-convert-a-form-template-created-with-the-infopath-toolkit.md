---
title: Ouverture ou conversion d'un modèle de formulaire créé avec InfoPath Toolkit
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
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Ouverture ou conversion d'un modèle de formulaire créé avec InfoPath Toolkit

Si vous avez créé un modèle de formulaire InfoPath 2003 avec code managé au moyen de l'un des kits de ressources InfoPath 2003 pour Visual Studio, pour assurer la compatibilité avec InfoPath 2003, vous pouvez continuer à travailler sur ce modèle de formulaire et poursuivre son développement en l'ouvrant dans Microsoft InfoPath ou Visual Studio 2012.
  
Vous pouvez également migrer et mettre à niveau le code dans votre projet InfoPath 2003 afin d'utiliser le nouveau modèle objet .NET fourni par l'espace de noms [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Lorsque vous procédez ainsi, tout le code doit être réécrit pour utiliser les membres de l'espace de noms **Microsoft. Office. InfoPath** , mais tout le code de votre projet précédent est conservé et entouré par **#if InfoPathManagedObjectModel** et **#endif **(C#) ou **#If modèle InfoPathManagedObject** , ainsi que les instructions **#End If** (Visual Basic) pour votre référence. 
  
Les procédures suivantes décrivent comment ouvrir un modèle de formulaire avec code managé créé à l'aide d'InfoPath Toolkit et assurer la compatibilité avec InfoPath 2003 ou migrer et mettre à niveau vers le nouveau modèle objet InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Ouvrir un modèle de formulaire avec code managé créé au moyen du kit de ressources InfoPath et conserver la compatibilité avec InfoPath 2003 au moyen de Visual Studio Tools for Applications

1. Ouvrez le Concepteur InfoPath, puis cliquez sur **ouvrir** dans l'onglet **fichier** . 
    
2. Dans la boîte de dialogue **ouvrir en mode création** , accédez au dossier du projet dans lequel est enregistré le projet de modèle de formulaire InfoPath Toolkit. 
    
    Par défaut, il s'agit d'un dossier `C:\Users\` dans *nom d'utilisateur* `\Documents\Visual Studio Projects` sur l'ordinateur sur lequel le projet a été créé.   ou, vous pouvez déplacer le dossier vers l'emplacement où InfoPath stocke les projets Visual Studio 2012, qui est `C:\Users\` par défaut *username*  `\Documents\InfoPath Projects`
    
3. Cliquez sur le fichier nommé manifest. xsf, puis cliquez sur **ouvrir**.
    
4. Sous l’onglet **Développeur**, cliquez sur **Éditeur de code**.
    
5. Le message suivant apparaît : « Vous devez enregistrer ce modèle de formulaire avant d'y ajouter du code Visual Basic ou C#. ». Cliquez sur **OK**pour continuer. 
    
6. Naviguez vers l'emplacement où vous voulez enregistrer le fichier, donnez un nom à celui-ci, puis cliquez sur **Enregistrer**.
    
7. Le message suivant apparaît : « Ce code a été créé avec un kit de ressources Microsoft Office InfoPath 2003 pour Microsoft Visual Studio. InfoPath doit migrer le projet de kit de ressources vers un nouveau format. ». Cliquez sur **OK** pour continuer. 
    
8. Sélectionnez le fichier de solution Visual Studio (. sln) pour le projet, puis cliquez sur **ouvrir**.
    
9. Le message suivant apparaît : « La migration de votre projet est terminée ». Cliquez sur **OK** pour continuer. 
    
10. Le message «le code de ce formulaire utilise le modèle objet InfoPath 2003» s'affiche avec l'invite «voulez-vous mettre à niveau votre code pour utiliser le modèle objet Microsoft Office InfoPath?» Cliquez sur **non** pour conserver la compatibilité avec InfoPath 2003 et continuer à travailler avec le modèle objet fourni par l'espace de noms [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
    
    Pour plus d'informations sur l'utilisation de modèles de formulaires avec code managé compatibles avec InfoPath 2003, voir [développement de modèles de formulaire à l'aide du modèle objet InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Ouvrir un modèle de formulaire avec code managé créé au moyen du kit de ressources InfoPath et le mettre à niveau pour qu’il utilise le nouveau modèle objet InfoPath au moyen de Visual Studio Tools for Applications

1. Ouvrez le Concepteur InfoPath, puis cliquez sur **ouvrir** dans l'onglet **fichier** . 
    
2. Sous **Ouvrir un modèle de formulaire**, cliquez sur **Sur mon ordinateur**.
    
3. Dans la boîte de dialogue **ouvrir en mode création** , accédez au dossier du projet dans lequel est enregistré le projet de modèle de formulaire InfoPath Toolkit. 
    
    Par défaut, il s'agit d'un `C:\Users\` dossier dans *nom d'utilisateur* `\Documents\Visual Studio Projects` sur l'ordinateur sur lequel le projet a été créé.   ou, vous pouvez déplacer le dossier vers l'emplacement où InfoPath stocke les projets Visual Studio 2012, qui est `C:\Users\` par défaut *username*  `\Documents\InfoPath Projects`
    
4. Cliquez sur le fichier nommé manifest. xsf, puis cliquez sur **ouvrir**.
    
5. Sous l’onglet **Développeur**, cliquez sur **Éditeur de code**.
    
6. Le message suivant apparaît : « Vous devez enregistrer ce modèle de formulaire avant d'y ajouter du code Visual Basic ou C#. ». Cliquez sur **OK**pour continuer. 
    
7. Naviguez vers l'emplacement où vous voulez enregistrer le fichier, donnez un nom à celui-ci, puis cliquez sur **Enregistrer**.
    
8. Le message suivant apparaît : « Ce code a été créé avec un kit de ressources Microsoft Office InfoPath 2003 pour Microsoft Visual Studio. InfoPath doit migrer le projet de kit de ressources vers un nouveau format. ». Cliquez sur **OK** pour continuer. 
    
9. Sélectionnez le fichier de solution Visual Studio (. sln) pour le projet, puis cliquez sur **ouvrir**.
    
10. Le message suivant apparaît : « La migration de votre projet est terminée ». Cliquez sur **OK** pour continuer. 
    
11. Le message «le code de ce formulaire utilise le modèle objet InfoPath 2003» s'affiche avec l'invite «voulez-vous mettre à niveau votre code pour utiliser le modèle objet Microsoft Office InfoPath?» Cliquez sur **Oui** pour mettre à niveau le modèle de formulaire afin d'utiliser le nouveau modèle objet de code managé fourni par l'espace de noms [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
    
    Votre code de formulaire est ouvert dans l'éditeur de code Visual Studio 2012 avec tout le code de votre projet précédent entouré par **#if** **InfoPathManagedObjectModel** et **#endif** (C#) ou **#If InfoPathManagedObjectModel** et **#End si **(Visual Basic) pour votre référence. L’ensemble de ce code devra être réécrit pour utiliser des membres du modèle objet fourni par l’espace de noms **Microsoft.Office.InfoPath**. 
    
    Pour plus d'informations sur l'utilisation de modèles de formulaires avec code managé qui utilisent le nouveau modèle objet InfoPath avec code managé, voir [développement de modèles de formulaire InfoPath avec code](developing-infopath-form-templates-with-code.md).
    

