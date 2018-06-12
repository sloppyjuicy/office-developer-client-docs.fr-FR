---
title: Présentation des formulaires entièrement fiables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath offre la possibilité de créer des formulaires entièrement fiables, c'est-à-dire des formulaires qui disposent des autorisations de sécurité supérieure et peuvent accéder à des ressources système et autres composants sur l’ordinateur d’un utilisateur. Cet article décrit la procédure est un formulaire entièrement fiable, et pourquoi il est utilisé et créer un formulaire entièrement fiable en convertissant manuellement et d’inscription d’un formulaire standard, ou à la signature numérique d’un formulaire standard.
ms.openlocfilehash: b410d5bee0080aae5e0af9687999595655b42edf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782464"
---
# <a name="understanding-fully-trusted-forms"></a>Présentation des formulaires entièrement fiables

InfoPath offre la possibilité de créer des formulaires entièrement fiables, c'est-à-dire des formulaires qui disposent des autorisations de sécurité supérieure et peuvent accéder à des ressources système et autres composants sur l’ordinateur d’un utilisateur. Cet article décrit la procédure est un formulaire entièrement fiable, et pourquoi il est utilisé et créer un formulaire entièrement fiable en convertissant manuellement et d’inscription d’un formulaire standard, ou à la signature numérique d’un formulaire standard.

Les modèles de formulaire InfoPath peuvent être déployés avec des niveaux de sécurité variables. Le niveau utilisé dépend du niveau d'accès aux ressources externes que vous voulez donner à un formulaire. Par défaut, les modèles de formulaire InfoPath ne peuvent pas accéder aux ressources système, ni utiliser de composant logiciel non marqué comme sécurisé pour l'exécution de script.
  
Pour qu'un formulaire soit utilisable, InfoPath doit pouvoir accéder au modèle de formulaire qui lui sert de base. Lorsque vous créez un modèle de formulaire, InfoPath crée une entrée dans le fichier de définition du formulaire (.xsf) qui contient l'URL de l'emplacement du modèle de formulaire. Un formulaire basé sur une URL est dit *en bac à sable*. Lorsqu'un utilisateur le remplit, le formulaire est ajouté à un cache local et n'a pas accès aux ressources système. Ce type de formulaire hérite ses autorisations du domaine dans lequel il est ouvert. 
  
Cependant, vous pouvez modifier un formulaire afin qu'il soit basé sur un nom URN (Uniform Resource Name), ce qui lui autorise l'accès aux ressources système. Formulaires de ce type sont appelés à être *entièrement fiable*. 
  
## <a name="why-use-a-fully-trusted-form"></a>Pourquoi utiliser un formulaire entièrement fiable ?

Les formulaires entièrement fiables disposent d'un meilleur ensemble d'autorisations que les formulaires en sandbox. Par exemple, ils peuvent contenir du code de programmation qui utilise des objets externes pour accéder aux ressources système. Ils peuvent utiliser des composants logiciels ou des contrôles Microsoft ActiveX non marqués comme sécurisés pour l'exécution de script et ils peuvent utiliser de la logique métier personnalisée, fournie par les assemblys .NET.
  
En outre, certains membres du modèle d'objet InfoPath sont définis avec le niveau de sécurité 3, ce qui signifie qu'ils ne sont utilisables que dans un formulaire entièrement fiable. Par exemple, pour accéder à l'objet Microsoft Office **CommandBars**, vous utilisez la propriété [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la classe InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) afin de lui définir une référence. Cette propriété étant définie avec un niveau de sécurité 3, elle ne peut être utilisée dans un formulaire qui n'est pas entièrement fiable. 
  
> [!NOTE]
> [!REMARQUE] Si vous utilisez la propriété [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ou tout autre membre du modèle d'objet doté d'un niveau de sécurité 3, dans un formulaire qui n'est pas entièrement fiable, le message d'erreur « autorisation refusée » s'affiche. 
  
## <a name="what-makes-a-form-fully-trusted"></a>Qu'est-ce qui rend un formulaire entièrement fiable ?

Les opérations suivantes, impliquant l'interface utilisateur InfoPath et les fichiers de formulaire, sont nécessaires pour créer et utiliser un formulaire entièrement fiable :
  
- Activation d'InfoPath pour permettre l'usage de formulaires entièrement fiables dans la catégorie **Éditeurs approuvés** de la boîte de dialogue **Centre de gestion de la confidentialité**. Cette option doit être activée afin que les utilisateurs puissent ouvrir les formulaires entièrement fiables. 
    
- Enregistrement du formulaire entièrement fiable sur l'ordinateur cible à l'aide de la méthode **RegisterSolution** de l'objet InfoPath **Application**. 
    
## <a name="creating-a-fully-trusted-form"></a>Création d'un formulaire entièrement fiable

- Vous pouvez créer le formulaire manuellement, ce qui implique la modification directe de certains fichiers du formulaire.
    
- Vous pouvez apposer une signature numérique sur le modèle de formulaire.
    
### <a name="manually-creating-a-fully-trusted-form"></a>Création manuelle d'un formulaire entièrement fiable

#### <a name="to-manually-create-a-fully-trusted-form"></a>Pour créer manuellement un formulaire entièrement fiable

1. Créez une copie de sauvegarde du modèle de formulaire que vous voulez rendre entièrement fiable.
    
2. Ouvrez le modèle de formulaire dans InfoPath.
    
3. Enregistrez les fichiers sources du formulaire dans un dossier sur votre disque dur en cliquant sur l'onglet **Fichier**, puis sur **Publier** et **Exporter les fichiers sources**.
    
4. Spécifiez le dossier dans lequel enregistrer les fichiers sources du formulaire, cliquez sur **OK** et quittez le concepteur InfoPath.
    
5. Dans le dossier dans lequel vous avez extrait les fichiers du formulaire, ouvrez le fichier de définition du formulaire (.xsf), intitulé  `manifest.xsf` par défaut, dans un éditeur de texte, tel que Microsoft Bloc-notes. 
    
6. Ajoutez les attributs suivants à l'élément **xDocumentClass** du fichier .xsf : 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!REMARQUE] Les valeurs utilisées pour le nom URN peuvent être une valeur de chaîne de quelconque sorte, du moment que cette valeur est unique. Il doit y avoir au moins deux valeurs après le `urn:` préfixe, ces valeurs doivent être séparées par un signe deux-points. En outre, le nom URN ne doit pas dépasser 255 caractères. 
  
7. Enregistrez et fermez le fichier .xsf, puis ouvrez le fichier de modèle XML (.xml) intitulé  `Template.xml` par défaut, dans un éditeur de texte, tel que Bloc-notes. 
    
8. Supprimez l'attribut **href** de l'instruction de traitement  `mso-infoPathSolution` et remplacez-le par le même attribut **name** utilisé à l'étape 6 pour le fichier .xsf. 
    
   > [!NOTE]
   > [!REMARQUE] Les valeurs URN utilisées pour l'attribut **name** doivent être identiques dans le fichier .xsf et le fichier du modèle XML. 
  
9. Enregistrez et fermez le fichier de modèle XML.
    
10. Regroupez les fichiers dans le fichier .xsn au format CAB à l'aide d'un outil tel que makecab.exe.
    
    > [!NOTE]
    > [!REMARQUE] Le concepteur de formulaire InfoPath prend en charge le regroupement de fichiers de formulaire en un fichier .xsn, cependant cette opération reconvertit le formulaire en formulaire basé sur une URL. Par conséquent, vous devez regrouper les fichiers manuellement pour éviter d'effacer les modifications que vous avez apportées aux fichiers du formulaire. 
  
11. Créez un programme d'installation personnalisé à l'aide de la méthode **RegisterSolution** dans l'objet InfoPath **Application** pour installer le formulaire entièrement fiable. Pour effectuer cette opération aisément, créez un fichier de script qui utilise les lignes de code ci-après (la syntaxe Microsoft JScript ou VBScript) : 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> [!REMARQUE] Cet exemple utilise un fichier de script simple, cependant vous pouvez également utiliser un mécanisme d'installation plus robuste, tel que les fichiers Microsoft Windows Installer (.msi). Cependant, assurez-vous d'utiliser la méthode **RegisterSolution** pour installer correctement le formulaire entièrement fiable sur l'ordinateur cible. Pour accéder à la méthode **RegisterSolution** de l'objet InfoPath **Application** de Visual Basic ou Visual Studio, définissez une référence pour la bibliothèque de types Microsoft InfoPath 3.0, fournie par le fichier IPEDITOR.dll installé dans le dossier C:\Program Files\Microsoft Office\Office14. 
  
Pour supprimer un formulaire entièrement fiable, utilisez la méthode **UnregisterSolution** de l'objet **Application**, comme illustré dans les exemples JScript et VBScript ci-après. 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a>Signature numérique d'un modèle de formulaire pour créer un formulaire entièrement fiable

Signature numérique d’un modèle de formulaire vous permet de déployer un modèle de formulaire entièrement fiable par courrier électronique ou sur un serveur Web, telle qu’un serveur qui exécute Microsoft SharePoint Foundation. Utilisez les étapes des trois procédures ci-après pour rendre un formulaire entièrement fiable en spécifiant la fiabilité totale pour le formulaire, en le signant numériquement et en le publiant.
  
#### <a name="to-digitally-sign-a-form-template"></a>Pour signer un modèle de formulaire numériquement

1. Ouvrez le formulaire dans le concepteur InfoPath, cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** dans l'onglet **Infos**. 
    
2. Dans la boîte de dialogue **Options de formulaire**, cliquez sur la catégorie **Sécurité et approbation**. 
    
3. Désactivez l'option **Déterminer automatiquement le niveau de sécurité (recommandé)**.
    
4. Sélectionnez **Confiance totale (le formulaire a accès aux fichiers et paramètres sur l'ordinateur de l'utilisateur)**.
    
5. Sous **Signature du modèle de formulaire**, sélectionnez **Signer ce modèle de formulaire**.
    
6. Cliquez sur **Sélectionner un certificat** pour sélectionner un certificat qui a été téléchargé auparavant et installé à partir d'un fournisseur de certificat approuvé. 
    
7. Cliquez sur OK deux fois pour quitter complètement.
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a>Pour publier le modèle de formulaire sur une bibliothèque de documents SharePoint

1. Cliquez sur l'onglet **Fichier**, puis sur **Publier** et **SharePoint Server**.
    
2. Suivez les instructions de l' **Assistant Publication** pour publier le modèle de formulaire sur une bibliothèque de documents SharePoint nouvelle ou existante. 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a>Pour créer un formulaire basé sur votre modèle de formulaire entièrement fiable et signé numériquement

1. Dans la bibliothèque de documents SharePoint, cliquez sur **Remplir un formulaire**.
    
   > [!NOTE]
   > [!REMARQUE] Une fois le modèle de formulaire publié sur une bibliothèque de documents SharePoint à l'aide de l' **Assistant Publication**, le modèle ne s'affiche pas en tant qu'élément dans la bibliothèque de formulaire. Lorsque vous créez un formulaire dans cette bibliothèque de documents, le modèle est utilisé par défaut en tant que modèle pour le nouveau formulaire. 
  
2. Si le modèle de formulaire par défaut a été signé numériquement, InfoPath affiche un avertissement de sécurité relatif au modèle de formulaire signé numériquement. Sélectionnez **Toujours faire confiance aux fichiers de cet éditeur et les ouvrir automatiquement**, puis cliquez sur **Ouvrir**.
    
## <a name="using-a-fully-trusted-form"></a>Utilisation d'un formulaire entièrement fiable

L'utilisation d'un formulaire entièrement fiable est très similaire à l'usage d'un formulaire standard. Les seules différences importantes sont que le formulaire peut accéder aux ressources limitées et les avertissements ne s'affichent plus.
  
> [!NOTE]
> Pour permettre à InfoPath d’utiliser un formulaire entièrement fiable, les utilisateurs doivent s’assurer que la case à cocher **Autoriser les formulaires entièrement fiables à exécuter sur mon ordinateur** est sélectionnée dans la catégorie **Éditeurs approuvés** de la boîte de dialogue **Centre de gestion de la confidentialité** . Pour ouvrir la boîte de dialogue **Centre de gestion de la confidentialité** , cliquez sur l’onglet **fichier** , cliquez sur **Options** (sous l’onglet **InfoPath** ), cliquez sur **Centre de gestion de la confidentialité**, puis cliquez sur **Paramètres du centre de gestion de la confidentialité**. 
  
Un formulaire entièrement fiable peut être ouvert dans InfoPath via la boîte de dialogue **Remplir un formulaire**. 
  
La boîte de dialogue **Remplir un formulaire** s'affiche lorsque vous cliquez sur **Formulaires supplémentaires** dans le volet des tâches **Remplir un formulaire** ou si vous cliquez sur la commande **Remplir un formulaire** dans le menu **Fichier**. 
  
### <a name="making-changes-to-a-fully-trusted-form"></a>Modification d'un formulaire entièrement fiable

Si vous devez modifier uniquement le fichier .xsn, vous pouvez demander aux utilisateurs de remplacer leur fichier .xsn existant par le nouveau, une fois les modifications effectuées. Ils n'auront pas à le réinstaller à l'aide d'un programme d'installation personnalisé.
  
Cependant, si vous modifiez les fichiers de formulaire contenus dans le fichier .xsn, vous devez regrouper les fichiers, tel que cela a été expliqué précédemment, puis demander aux utilisateurs de réinstaller le formulaire entièrement fiable.
  
> [!NOTE]
> [!REMARQUE] La meilleure méthode est de réenregistrer le modèle de formulaire au format .xsn via le concepteur InfoPath, puis de suivre les étapes indiquées dans cet article pour créer un formulaire entièrement fiable. 
  
## <a name="conclusion"></a>Conclusion

Selon les besoins de votre entreprise et ceux de vos utilisateurs, vous devrez peut-être créer un formulaire doté d'un ensemble d'autorisations meilleur que celui du formulaire InfoPath standard. InfoPath permet de modifier un formulaire afin qu'il accède aux ressources système et à d'autres ressources externes qui ne sont pas marquées comme sécurisées pour l'exécution de script. Cette opération peut être effectuée manuellement en modifiant les fichiers de formulaire contenus dans un modèle de formulaire et en exécutant un script d'installation ou en signant numériquement le modèle du formulaire.
  

