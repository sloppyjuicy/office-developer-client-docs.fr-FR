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
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="30afe-104">Présentation des formulaires entièrement fiables</span><span class="sxs-lookup"><span data-stu-id="30afe-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="30afe-105">InfoPath offre la possibilité de créer des formulaires entièrement fiables, c'est-à-dire des formulaires qui disposent des autorisations de sécurité supérieure et peuvent accéder à des ressources système et autres composants sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30afe-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="30afe-106">Cet article décrit la procédure est un formulaire entièrement fiable, et pourquoi il est utilisé et créer un formulaire entièrement fiable en convertissant manuellement et d’inscription d’un formulaire standard, ou à la signature numérique d’un formulaire standard.</span><span class="sxs-lookup"><span data-stu-id="30afe-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="30afe-p103">Les modèles de formulaire InfoPath peuvent être déployés avec des niveaux de sécurité variables. Le niveau utilisé dépend du niveau d'accès aux ressources externes que vous voulez donner à un formulaire. Par défaut, les modèles de formulaire InfoPath ne peuvent pas accéder aux ressources système, ni utiliser de composant logiciel non marqué comme sécurisé pour l'exécution de script.</span><span class="sxs-lookup"><span data-stu-id="30afe-p103">InfoPath form templates can be deployed with varying levels of security. The level you use is dictated by the level of access to external resources that you want a form to have. By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting. However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="30afe-111">Pour qu'un formulaire soit utilisable, InfoPath doit pouvoir accéder au modèle de formulaire qui lui sert de base.</span><span class="sxs-lookup"><span data-stu-id="30afe-111">For a form to be used, InfoPath must be able to access the form template that the form is based on.</span></span> <span data-ttu-id="30afe-112">Lorsque vous créez un modèle de formulaire, InfoPath crée une entrée dans le fichier de définition du formulaire (.xsf) qui contient l'URL de l'emplacement du modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-112">When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template.</span></span> <span data-ttu-id="30afe-113">Un formulaire basé sur une URL est dit *en bac à sable*.</span><span class="sxs-lookup"><span data-stu-id="30afe-113">A URL-based form is said to be *sandboxed*.</span></span> <span data-ttu-id="30afe-114">Lorsqu'un utilisateur le remplit, le formulaire est ajouté à un cache local et n'a pas accès aux ressources système.</span><span class="sxs-lookup"><span data-stu-id="30afe-114">When a user fills it out, the form is added in a local cache and denied access to system resources.</span></span> <span data-ttu-id="30afe-115">Ce type de formulaire hérite ses autorisations du domaine dans lequel il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="30afe-115">This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="30afe-116">Cependant, vous pouvez modifier un formulaire afin qu'il soit basé sur un nom URN (Uniform Resource Name), ce qui lui autorise l'accès aux ressources système.</span><span class="sxs-lookup"><span data-stu-id="30afe-116">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources.</span></span> <span data-ttu-id="30afe-117">Formulaires de ce type sont appelés à être *entièrement fiable*.</span><span class="sxs-lookup"><span data-stu-id="30afe-117">Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="30afe-118">Pourquoi utiliser un formulaire entièrement fiable ?</span><span class="sxs-lookup"><span data-stu-id="30afe-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="30afe-p106">Les formulaires entièrement fiables disposent d'un meilleur ensemble d'autorisations que les formulaires en sandbox. Par exemple, ils peuvent contenir du code de programmation qui utilise des objets externes pour accéder aux ressources système. Ils peuvent utiliser des composants logiciels ou des contrôles Microsoft ActiveX non marqués comme sécurisés pour l'exécution de script et ils peuvent utiliser de la logique métier personnalisée, fournie par les assemblys .NET.</span><span class="sxs-lookup"><span data-stu-id="30afe-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="30afe-p107">En outre, certains membres du modèle d'objet InfoPath sont définis avec le niveau de sécurité 3, ce qui signifie qu'ils ne sont utilisables que dans un formulaire entièrement fiable. Par exemple, pour accéder à l'objet Microsoft Office **CommandBars**, vous utilisez la propriété [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la classe InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) afin de lui définir une référence. Cette propriété étant définie avec un niveau de sécurité 3, elle ne peut être utilisée dans un formulaire qui n'est pas entièrement fiable.</span><span class="sxs-lookup"><span data-stu-id="30afe-p107">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form. For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it. Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30afe-124">Si vous utilisez la propriété [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ou tout autre membre du modèle d'objet doté d'un niveau de sécurité 3, dans un formulaire qui n'est pas entièrement fiable, le message d'erreur « autorisation refusée » s'affiche.</span><span class="sxs-lookup"><span data-stu-id="30afe-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="30afe-125">Qu'est-ce qui rend un formulaire entièrement fiable ?</span><span class="sxs-lookup"><span data-stu-id="30afe-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="30afe-126">Les opérations suivantes, impliquant l'interface utilisateur InfoPath et les fichiers de formulaire, sont nécessaires pour créer et utiliser un formulaire entièrement fiable :</span><span class="sxs-lookup"><span data-stu-id="30afe-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="30afe-p108">Activation d'InfoPath pour permettre l'usage de formulaires entièrement fiables dans la catégorie **Éditeurs approuvés** de la boîte de dialogue **Centre de gestion de la confidentialité**. Cette option doit être activée afin que les utilisateurs puissent ouvrir les formulaires entièrement fiables.</span><span class="sxs-lookup"><span data-stu-id="30afe-p108">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box. This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="30afe-129">Enregistrement du formulaire entièrement fiable sur l'ordinateur cible à l'aide de la méthode **RegisterSolution** de l'objet InfoPath **Application**.</span><span class="sxs-lookup"><span data-stu-id="30afe-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="30afe-130">Création d'un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="30afe-131">Vous pouvez créer le formulaire manuellement, ce qui implique la modification directe de certains fichiers du formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="30afe-132">Vous pouvez apposer une signature numérique sur le modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="30afe-133">Création manuelle d'un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="30afe-134">Pour créer manuellement un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="30afe-135">Créez une copie de sauvegarde du modèle de formulaire que vous voulez rendre entièrement fiable.</span><span class="sxs-lookup"><span data-stu-id="30afe-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="30afe-136">Ouvrez le modèle de formulaire dans InfoPath.</span><span class="sxs-lookup"><span data-stu-id="30afe-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="30afe-137">Enregistrez les fichiers sources du formulaire dans un dossier sur votre disque dur en cliquant sur l'onglet **Fichier**, puis sur **Publier** et **Exporter les fichiers sources**.</span><span class="sxs-lookup"><span data-stu-id="30afe-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="30afe-138">Spécifiez le dossier dans lequel enregistrer les fichiers sources du formulaire, cliquez sur **OK** et quittez le concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="30afe-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="30afe-139">Dans le dossier dans lequel vous avez extrait les fichiers du formulaire, ouvrez le fichier de définition du formulaire (.xsf), intitulé  `manifest.xsf` par défaut, dans un éditeur de texte, tel que Microsoft Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="30afe-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="30afe-140">Ajoutez les attributs suivants à l'élément **xDocumentClass** du fichier .xsf :</span><span class="sxs-lookup"><span data-stu-id="30afe-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!REMARQUE] Les valeurs utilisées pour le nom URN peuvent être une valeur de chaîne de quelconque sorte, du moment que cette valeur est unique. Il doit y avoir au moins deux valeurs après le `urn:` préfixe, ces valeurs doivent être séparées par un signe deux-points. <span data-ttu-id="30afe-143">En outre, le nom URN ne doit pas dépasser 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="30afe-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="30afe-144">Enregistrez et fermez le fichier .xsf, puis ouvrez le fichier de modèle XML (.xml) intitulé  `Template.xml` par défaut, dans un éditeur de texte, tel que Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="30afe-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="30afe-145">Supprimez l'attribut **href** de l'instruction de traitement  `mso-infoPathSolution` et remplacez-le par le même attribut **name** utilisé à l'étape 6 pour le fichier .xsf.</span><span class="sxs-lookup"><span data-stu-id="30afe-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="30afe-146">Les valeurs URN utilisées pour l'attribut **name** doivent être identiques dans le fichier .xsf et le fichier du modèle XML.</span><span class="sxs-lookup"><span data-stu-id="30afe-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="30afe-147">Enregistrez et fermez le fichier de modèle XML.</span><span class="sxs-lookup"><span data-stu-id="30afe-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="30afe-148">Regroupez les fichiers dans le fichier .xsn au format CAB à l'aide d'un outil tel que makecab.exe.</span><span class="sxs-lookup"><span data-stu-id="30afe-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="30afe-p110">Le concepteur de formulaire InfoPath prend en charge le regroupement de fichiers de formulaire en un fichier .xsn, cependant cette opération reconvertit le formulaire en formulaire basé sur une URL. Par conséquent, vous devez regrouper les fichiers manuellement pour éviter d'effacer les modifications que vous avez apportées aux fichiers du formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="30afe-p111">Créez un programme d'installation personnalisé à l'aide de la méthode **RegisterSolution** dans l'objet InfoPath **Application** pour installer le formulaire entièrement fiable. Pour effectuer cette opération aisément, créez un fichier de script qui utilise les lignes de code ci-après (la syntaxe Microsoft JScript ou VBScript) :</span><span class="sxs-lookup"><span data-stu-id="30afe-p111">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form. A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
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
> <span data-ttu-id="30afe-p112">Cet exemple utilise un fichier de script simple, cependant vous pouvez également utiliser un mécanisme d'installation plus robuste, tel que les fichiers Microsoft Windows Installer (.msi). Cependant, assurez-vous d'utiliser la méthode **RegisterSolution** pour installer correctement le formulaire entièrement fiable sur l'ordinateur cible. Pour accéder à la méthode **RegisterSolution** de l'objet InfoPath **Application** de Visual Basic ou Visual Studio, définissez une référence pour la bibliothèque de types Microsoft InfoPath 3.0, fournie par le fichier IPEDITOR.dll installé dans le dossier C:\Program Files\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="30afe-p112">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files. Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer. To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="30afe-156">Pour supprimer un formulaire entièrement fiable, utilisez la méthode **UnregisterSolution** de l'objet **Application**, comme illustré dans les exemples JScript et VBScript ci-après.</span><span class="sxs-lookup"><span data-stu-id="30afe-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
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

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="30afe-157">Signature numérique d'un modèle de formulaire pour créer un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="30afe-158">Signature numérique d’un modèle de formulaire vous permet de déployer un modèle de formulaire entièrement fiable par courrier électronique ou sur un serveur Web, telle qu’un serveur qui exécute Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="30afe-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="30afe-159">Utilisez les étapes des trois procédures ci-après pour rendre un formulaire entièrement fiable en spécifiant la fiabilité totale pour le formulaire, en le signant numériquement et en le publiant.</span><span class="sxs-lookup"><span data-stu-id="30afe-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="30afe-160">Pour signer un modèle de formulaire numériquement</span><span class="sxs-lookup"><span data-stu-id="30afe-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="30afe-161">Ouvrez le formulaire dans le concepteur InfoPath, cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** dans l'onglet **Infos**.</span><span class="sxs-lookup"><span data-stu-id="30afe-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="30afe-162">Dans la boîte de dialogue **Options de formulaire**, cliquez sur la catégorie **Sécurité et approbation**.</span><span class="sxs-lookup"><span data-stu-id="30afe-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="30afe-163">Désactivez l'option **Déterminer automatiquement le niveau de sécurité (recommandé)**.</span><span class="sxs-lookup"><span data-stu-id="30afe-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="30afe-164">Sélectionnez **Confiance totale (le formulaire a accès aux fichiers et paramètres sur l'ordinateur de l'utilisateur)**.</span><span class="sxs-lookup"><span data-stu-id="30afe-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="30afe-165">Sous **Signature du modèle de formulaire**, sélectionnez **Signer ce modèle de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="30afe-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="30afe-166">Cliquez sur **Sélectionner un certificat** pour sélectionner un certificat qui a été téléchargé auparavant et installé à partir d'un fournisseur de certificat approuvé.</span><span class="sxs-lookup"><span data-stu-id="30afe-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="30afe-167">Cliquez sur OK deux fois pour quitter complètement.</span><span class="sxs-lookup"><span data-stu-id="30afe-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="30afe-168">Pour publier le modèle de formulaire sur une bibliothèque de documents SharePoint</span><span class="sxs-lookup"><span data-stu-id="30afe-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="30afe-169">Cliquez sur l'onglet **Fichier**, puis sur **Publier** et **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="30afe-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="30afe-170">Suivez les instructions de l' **Assistant Publication** pour publier le modèle de formulaire sur une bibliothèque de documents SharePoint nouvelle ou existante.</span><span class="sxs-lookup"><span data-stu-id="30afe-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="30afe-171">Pour créer un formulaire basé sur votre modèle de formulaire entièrement fiable et signé numériquement</span><span class="sxs-lookup"><span data-stu-id="30afe-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="30afe-172">Dans la bibliothèque de documents SharePoint, cliquez sur **Remplir un formulaire**.</span><span class="sxs-lookup"><span data-stu-id="30afe-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="30afe-p114">Une fois le modèle de formulaire publié sur une bibliothèque de documents SharePoint à l'aide de l' **Assistant Publication**, le modèle ne s'affiche pas en tant qu'élément dans la bibliothèque de formulaire. Lorsque vous créez un formulaire dans cette bibliothèque de documents, le modèle est utilisé par défaut en tant que modèle pour le nouveau formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-p114">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library. When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="30afe-p115">Si le modèle de formulaire par défaut a été signé numériquement, InfoPath affiche un avertissement de sécurité relatif au modèle de formulaire signé numériquement. Sélectionnez **Toujours faire confiance aux fichiers de cet éditeur et les ouvrir automatiquement**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="30afe-p115">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template. Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="30afe-177">Utilisation d'un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="30afe-p116">L'utilisation d'un formulaire entièrement fiable est très similaire à l'usage d'un formulaire standard. Les seules différences importantes sont que le formulaire peut accéder aux ressources limitées et les avertissements ne s'affichent plus.</span><span class="sxs-lookup"><span data-stu-id="30afe-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30afe-180">Pour permettre à InfoPath d’utiliser un formulaire entièrement fiable, les utilisateurs doivent s’assurer que la case à cocher **Autoriser les formulaires entièrement fiables à exécuter sur mon ordinateur** est sélectionnée dans la catégorie **Éditeurs approuvés** de la boîte de dialogue **Centre de gestion de la confidentialité** .</span><span class="sxs-lookup"><span data-stu-id="30afe-180">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="30afe-181">Pour ouvrir la boîte de dialogue **Centre de gestion de la confidentialité** , cliquez sur l’onglet **fichier** , cliquez sur **Options** (sous l’onglet **InfoPath** ), cliquez sur **Centre de gestion de la confidentialité**, puis cliquez sur **Paramètres du centre de gestion de la confidentialité**.</span><span class="sxs-lookup"><span data-stu-id="30afe-181">To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="30afe-182">Un formulaire entièrement fiable peut être ouvert dans InfoPath via la boîte de dialogue **Remplir un formulaire**.</span><span class="sxs-lookup"><span data-stu-id="30afe-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="30afe-183">La boîte de dialogue **Remplir un formulaire** s'affiche lorsque vous cliquez sur **Formulaires supplémentaires** dans le volet des tâches **Remplir un formulaire** ou si vous cliquez sur la commande **Remplir un formulaire** dans le menu **Fichier**.</span><span class="sxs-lookup"><span data-stu-id="30afe-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="30afe-184">Modification d'un formulaire entièrement fiable</span><span class="sxs-lookup"><span data-stu-id="30afe-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="30afe-p118">Si vous devez modifier uniquement le fichier .xsn, vous pouvez demander aux utilisateurs de remplacer leur fichier .xsn existant par le nouveau, une fois les modifications effectuées. Ils n'auront pas à le réinstaller à l'aide d'un programme d'installation personnalisé.</span><span class="sxs-lookup"><span data-stu-id="30afe-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="30afe-187">Cependant, si vous modifiez les fichiers de formulaire contenus dans le fichier .xsn, vous devez regrouper les fichiers, tel que cela a été expliqué précédemment, puis demander aux utilisateurs de réinstaller le formulaire entièrement fiable.</span><span class="sxs-lookup"><span data-stu-id="30afe-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30afe-188">La meilleure méthode est de réenregistrer le modèle de formulaire au format .xsn via le concepteur InfoPath, puis de suivre les étapes indiquées dans cet article pour créer un formulaire entièrement fiable.</span><span class="sxs-lookup"><span data-stu-id="30afe-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="30afe-189">Conclusion</span><span class="sxs-lookup"><span data-stu-id="30afe-189">Conclusion</span></span>

<span data-ttu-id="30afe-p119">Selon les besoins de votre entreprise et ceux de vos utilisateurs, vous devrez peut-être créer un formulaire doté d'un ensemble d'autorisations meilleur que celui du formulaire InfoPath standard. InfoPath permet de modifier un formulaire afin qu'il accède aux ressources système et à d'autres ressources externes qui ne sont pas marquées comme sécurisées pour l'exécution de script. Cette opération peut être effectuée manuellement en modifiant les fichiers de formulaire contenus dans un modèle de formulaire et en exécutant un script d'installation ou en signant numériquement le modèle du formulaire.</span><span class="sxs-lookup"><span data-stu-id="30afe-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

