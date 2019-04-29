---
title: Aperçu et déBogage des modèles de formulaire InfoPath avec code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath avec Visual Studio 2012 permet le débogage en exécutant le code du formulaire en mode Aperçu. Lorsque vous commencez à déboguer le code du formulaire, votre projet est compilé et InfoPath affiche votre formulaire dans la fenêtre d'aperçu InfoPath. Lors du passage sur une ligne de code contenant un point d'arrêt, le focus passe dans l'Éditeur de code. Si vous continuez au-delà d'un point d'arrêt, le focus repasse dans la fenêtre d'aperçu. Le débogage s'arrête lorsque vous fermez la fenêtre d'aperçu.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405239"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="79154-108">Aperçu et déBogage des modèles de formulaire InfoPath avec code</span><span class="sxs-lookup"><span data-stu-id="79154-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="79154-p102">Microsoft InfoPath avec Visual Studio 2012 permet le débogage en exécutant le code du formulaire en mode Aperçu. Lorsque vous commencez à déboguer le code du formulaire, votre projet est compilé et InfoPath affiche votre formulaire dans la fenêtre d'aperçu InfoPath. Lors du passage sur une ligne de code contenant un point d'arrêt, le focus passe dans l'Éditeur de code. Si vous continuez au-delà d'un point d'arrêt, le focus repasse dans la fenêtre d'aperçu. Le débogage s'arrête lorsque vous fermez la fenêtre d'aperçu.</span><span class="sxs-lookup"><span data-stu-id="79154-p102">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode. When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window. When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor. When you continue past a breakpoint, the focus moves back to the preview window. Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="79154-114">Vous pouvez également modifier les options de formulaire du modèle de formulaire dont vous souhaitez afficher un aperçu et que vous voulez déboguer en utilisant un rôle utilisateur spécifique, un fichier de données exemple ou en spécifiant le domaine dans lequel le formulaire sera publié.</span><span class="sxs-lookup"><span data-stu-id="79154-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="79154-115">[!REMARQUE] Il n'est pas possible de déboguer les modèles de formulaires après leur déploiement au moment de l'exécution à partir des Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="79154-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="79154-116">Cela comprend les modèles de formulaires qui sont compatibles uniquement avec InfoPath, ainsi que ceux qui sont compatibles avec InfoPath et le navigateur Web utilisant InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="79154-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="79154-117">Cependant, vous pouvez enregistrer des valeurs dans un champ à partir du code à l'exécution pour vous aider à résoudre les problèmes de la logique métier d'un modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="79154-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="79154-118">Pour plus d'informations sur la façon de procéder, consultez la rubrique [enregistrer des valeurs dans un champ pour](how-to-log-values-to-a-field-for-debugging.md)le débogage.</span><span class="sxs-lookup"><span data-stu-id="79154-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="79154-119">Débogage en mode Aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="79154-120">Pour déboguer un projet InfoPath en mode Aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="79154-121">Créez ou ouvrez un modèle de formulaire InfoPath avec code managé dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="79154-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="79154-122">Définissez un ou plusieurs points d'arrêt dans votre code de formulaire dans l'éditeur de code en cliquant sur la barre grise à gauche de la ligne de code où vous voulez insérer un point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="79154-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="79154-123">Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution marquera une pause à ce point d'arrêt dans votre code de formulaire.</span><span class="sxs-lookup"><span data-stu-id="79154-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="79154-124">Dans le menu **Débogage**, cliquez sur **Démarrer le débogage**; ou appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="79154-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="79154-125">Le projet est compilé et le formulaire s'affiche dans la fenêtre d'aperçu.</span><span class="sxs-lookup"><span data-stu-id="79154-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="79154-126">Utilisez le formulaire jusqu'à ce que vous rencontriez une ligne contenant un point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="79154-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="79154-127">Le focus revient dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="79154-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="79154-128">Dans le menu **Débogage**, cliquez sur **Continuer** ou appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="79154-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="79154-129">Lorsque vous avez terminé le débogage, fermez la fenêtre d'aperçu ou, dans le menu **Débogage**, cliquez sur **Arrêter le débogage**.</span><span class="sxs-lookup"><span data-stu-id="79154-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="79154-130">Pour déboguer un modèle de formulaire InfoPath avec code managé lors de l'utilisation d'un membre du modèle objet nécessitant une confiance totale, vous devez configurer votre modèle de formulaire comme décrit dans [Aperçu et débogage des modèles de formulaire qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="79154-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="79154-131">Utilisation d'un fichier exemple de données</span><span class="sxs-lookup"><span data-stu-id="79154-131">Using a Sample Data File</span></span>

<span data-ttu-id="79154-p104">Par défaut, le débogage et l'aperçu utilisent le fichier template.xml créé lors de la création d'un modèle de formulaire. Vous pouvez créer votre propre fichier de données et en spécifier l'utilisation lors de l'aperçu ou du débogage en suivant l'une des procédures ci-dessous. </span><span class="sxs-lookup"><span data-stu-id="79154-p104">By default, debugging and previewing uses the template.xml file that is created when a form template is created. You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="79154-134">Pour spécifier un fichier exemple de données à utiliser pour le débogage ou l'aperçu dans Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="79154-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="79154-135">Pour afficher template.xml, ouvrez le modèle de formulaire en mode Création dans InfoPath.</span><span class="sxs-lookup"><span data-stu-id="79154-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="79154-136">Cliquez sur l'onglet **Fichier**, cliquez sur **Enregistrement**, sur **Enregistrer le modèle de formulaire sous**, puis cliquez sur **Fichiers source**.</span><span class="sxs-lookup"><span data-stu-id="79154-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="79154-137">Enregistrez les fichiers du modèle de formulaire dans un dossier, puis ouvrez le fichier template.xml dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="79154-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="79154-138">Créez et enregistrez un fichier avec la même structure que template.xml avec les données exemple que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="79154-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="79154-139">Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos**.</span><span class="sxs-lookup"><span data-stu-id="79154-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="79154-140">Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis sous **Exemple de données** spécifiez le fichier exemple que vous avez créé dans la zone **Emplacement du fichier**.</span><span class="sxs-lookup"><span data-stu-id="79154-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="79154-141">Spécification d'un rôle d'utilisateur à utiliser lors du débogage ou de l'affichage de l'aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="79154-p105">Si le formulaire dans lequel vous travaillez contient des rôles d'utilisateur, vous pouvez spécifier le rôle d'utilisateur à utiliser lors du débogage ou de l'aperçu du formulaire. Pour plus d'informations sur la définition des rôles d'utilisateur, recherchez « Rôle d'utilisateur » dans l'aide d'InfoPath.</span><span class="sxs-lookup"><span data-stu-id="79154-p105">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form. For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="79154-p106">[!REMARQUE] L'option permettant de spécifier un rôle d'utilisateur n'est pas disponible si la compatibilité de votre modèle de formulaire est paramétrée comme **Formulaires de navigateur Web**. Les rôles des utilisateurs ne sont pas pris en charge dans les modèles de formulaires ouverts dans le navigateur à partir d'InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="79154-p106">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**. User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="79154-146">Pour spécifier un rôle à utiliser pour le débogage ou l'aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="79154-147">Si vous travaillez dans Visual Studio 2012, basculez vers le Concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="79154-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="79154-148">Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**.</span><span class="sxs-lookup"><span data-stu-id="79154-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="79154-149">Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis spécifiez le rôle d'utilisateur à utiliser dans la zone de liste déroulante **Aperçu en tant que**.</span><span class="sxs-lookup"><span data-stu-id="79154-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="79154-150">Spécification d'un domaine à utiliser lors du débogage ou de l'affichage de l'aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="79154-p107">Vous pouvez afficher un aperçu d'un formulaire comme s'il avait été publié dans un domaine spécifique. Ce paramètre fonctionne uniquement si le niveau de sécurité du modèle de formulaire est explicitement défini sur **Domaine**.</span><span class="sxs-lookup"><span data-stu-id="79154-p107">You can preview a form as if it was published to a specific domain. This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="79154-153">Pour spécifier un domaine à utiliser pour le débogage ou l'aperçu</span><span class="sxs-lookup"><span data-stu-id="79154-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="79154-154">Si vous travaillez dans Visual Studio 2012, basculez vers le Concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="79154-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="79154-155">Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**.</span><span class="sxs-lookup"><span data-stu-id="79154-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="79154-156">Cliquez sur la catégorie **Aperçu** de la boîte de dialogue **Options de formulaire**, puis spécifiez le domaine à utiliser lors de l'aperçu ou du débogage dans la zone **Domaine**.</span><span class="sxs-lookup"><span data-stu-id="79154-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="79154-157">Cliquez sur la catégorie **Sécurité et approbation** de la boîte de dialogue **Options de formulaire**, désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**, puis cliquez sur **Domaine**.</span><span class="sxs-lookup"><span data-stu-id="79154-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

