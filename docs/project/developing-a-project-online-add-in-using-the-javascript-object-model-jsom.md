---
title: Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit le complément Microsoft Project Online développement afin d’améliorer votre expérience avec Project Online. Le projet de développement est implémenté comme une procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’atteindre de récupérer les tâches associées à des projets individuels.
ms.openlocfilehash: 91d475afd5c4085b00ed06b66620f0d18174fd7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787797"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="531a8-105">Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="531a8-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="531a8-106">Cet article décrit le complément Microsoft Project Online développement afin d’améliorer votre expérience avec Project Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="531a8-107">Le projet de développement est implémenté comme une procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="531a8-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="531a8-108">Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’atteindre de récupérer les tâches associées à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="531a8-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="531a8-109">Au moment de l’exécution, la liste de compléments ressemble à l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="531a8-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="531a8-110">![Capture d’écran montrant une liste de tâches et des projets JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Capture d’écran montrant une liste de tâches et des projets JSOM")</span><span class="sxs-lookup"><span data-stu-id="531a8-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="531a8-111">L’objectif de l’exemple est l’interaction avec le Project Online, rendant des requêtes et en définissant le contexte de chaque demande à partir du service.</span><span class="sxs-lookup"><span data-stu-id="531a8-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="531a8-112">Des éléments de l’interface utilisateur d’une attention minimal.</span><span class="sxs-lookup"><span data-stu-id="531a8-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="531a8-113">Au lieu de cela, les listes source fournissent des commentaires relatifs à l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="531a8-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="531a8-114">Les fichiers source pour le complément logiciel exemple, un projet Visual Studio, sont disponibles à : https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span><span class="sxs-lookup"><span data-stu-id="531a8-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="531a8-115">Conserver les fichiers source pratique comme référence pendant la lecture de l’article, comme chacun vient s’ajouter à l’autre.</span><span class="sxs-lookup"><span data-stu-id="531a8-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="531a8-116">Les fichiers dans Visual Studio project build et peuvent être exécutées avec peu de modifications, en remplaçant l’URL de votre client Project Online jusqu’au dossier PWA.</span><span class="sxs-lookup"><span data-stu-id="531a8-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="531a8-117">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="531a8-117">Background</span></span>

<span data-ttu-id="531a8-118">Project Online est un service d’Office 365 qui permet aux entreprises une solution project management office (PMO) pour coordonner et gérer des portefeuilles, programmes et projets et de gestion de portefeuille de projets (PPM).</span><span class="sxs-lookup"><span data-stu-id="531a8-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="531a8-119">Project Online est une offre différente versions de bureau de projet ; encore, Project Online toujours contient les fonctionnalités pour mettre à jour et suivre les détails du projet dans toute la durée de vie d’un projet.</span><span class="sxs-lookup"><span data-stu-id="531a8-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="531a8-120">Project Online repose sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="531a8-121">Un complément Project Online hébergé se compose des fichiers JavaScript et des ressources qui interagissent avec l’API côté Client-modèle objet.</span><span class="sxs-lookup"><span data-stu-id="531a8-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="531a8-122">Lorsque l’utilisateur visite la macro complémentaire, le JavaScript et les ressources sont téléchargés et exécutées dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="531a8-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="531a8-123">Le complément effectue des appels asynchrones vers Project Online pour interagir avec le service, si la création, la récupération, mise à jour ou suppression de données.</span><span class="sxs-lookup"><span data-stu-id="531a8-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="531a8-124">Project Online effectue une action supplémentaire pour protéger les informations appartenant à d’autres clients à partir de la macro complémentaire ; à savoir, Project Online crée un site isolé pour interagir avec les demandes à partir de la macro complémentaire.</span><span class="sxs-lookup"><span data-stu-id="531a8-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="531a8-125">Pas de code personnalisé s’exécute sur l’hôte de Project Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="531a8-126">Le paramétrage de développement pour Project Online compléments utilise le type de projet Visual Studio SharePoint Add-in.</span><span class="sxs-lookup"><span data-stu-id="531a8-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="531a8-127">Le complément est écrit en JavaScript et utilise le modèle d’objet Project JavaScript (JSOM) pour interagir avec le service de Project Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="531a8-128">Le JSOM hérite la plupart de ses fonctionnalités du JSOM SharePoint.</span><span class="sxs-lookup"><span data-stu-id="531a8-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="531a8-129">Compléments peuvent être publiés et vendus dans l’Office Store ou déployés dans un catalogue d’applications privé sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="531a8-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="531a8-130">Pour plus d’informations, voir [déployer et publier votre complément Office](http://dev.office.com/docs/add-ins/publish/publish.aspx).</span><span class="sxs-lookup"><span data-stu-id="531a8-130">For more information, see [Deploy and publish your Office Add-in](http://dev.office.com/docs/add-ins/publish/publish.aspx).</span></span> <span data-ttu-id="531a8-131">> Le complément utilisé dans cet article est un exemple pour les développeurs ; elle n’est pas destinée à utiliser dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="531a8-131">> The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="531a8-132">Le principal objectif consiste à afficher un exemple de développement d’applications pour Project Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="531a8-133">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="531a8-133">Prerequisites</span></span>

<span data-ttu-id="531a8-134">Dans un environnement Windows pris en charge, ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="531a8-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="531a8-135">**.NET framework 4.0 ou version ultérieure**: les versions complètes de l’infrastructure de la version 4.0 sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="531a8-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="531a8-136">Le site de téléchargement est https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-136">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="531a8-137">**Visual Studio 2013 ou version ultérieure**:</span><span class="sxs-lookup"><span data-stu-id="531a8-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="531a8-138">L’édition professionnelle de Visual Studio 2015 est prête à commencer la mise à l’emploi et est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="531a8-139">L’édition de la Communauté de Visual Studio 2015 est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="531a8-140">Cette édition nécessite une installation manuelle des outils de développement Microsoft Office pour Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="531a8-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="531a8-141">Les outils de développement Microsoft Office pour Visual Studio sont disponibles sur https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="531a8-142">**Compte A Project Online**: Cela permet d’accéder au service d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="531a8-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="531a8-143">Pour plus d’informations sur l’obtention d’un compte Project Online, voir https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="531a8-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="531a8-144">Assurez-vous que l’utilisateur dispose d’autorisations suffisantes pour accéder à des projets dans le client Project Online.</span><span class="sxs-lookup"><span data-stu-id="531a8-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="531a8-145">**Projets sur le site d’hébergement** sont remplies avec les informations.</span><span class="sxs-lookup"><span data-stu-id="531a8-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="531a8-146">La norme .NET Framework est l’infrastructure correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="531a8-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="531a8-147">N’utilisez pas le « .NET Framework 4 Client Profile ».</span><span class="sxs-lookup"><span data-stu-id="531a8-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="531a8-148">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="531a8-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="531a8-149">Configuration de l’application se compose de création d’un nouveau projet, lier les bibliothèques appropriées et déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="531a8-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="531a8-150">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="531a8-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="531a8-151">La section est brève et très simple.</span><span class="sxs-lookup"><span data-stu-id="531a8-151">The section is brief and very basic.</span></span> <span data-ttu-id="531a8-152">La valeur a les informations est fusionné dans un seul endroit.</span><span class="sxs-lookup"><span data-stu-id="531a8-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="531a8-153">Sélectionnez le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="531a8-153">Select a Visual Studio project</span></span>

<span data-ttu-id="531a8-154">Pour créer un projet de type approprié pour le complément, vous devez effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="531a8-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="531a8-155">Mots clés rencontrés dans l’écran ont un attribut **gras** :</span><span class="sxs-lookup"><span data-stu-id="531a8-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="531a8-156">Dans le menu fichier, choisissez **fichier** > **New** > **Project**.</span><span class="sxs-lookup"><span data-stu-id="531a8-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="531a8-157">À partir des modèles installés dans le volet gauche, sélectionnez **c#** > **Office/SharePoint** > **Web Add-ins**.</span><span class="sxs-lookup"><span data-stu-id="531a8-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="531a8-158">En haut du volet central, sélectionnez **.NET Framework 4** ou version ultérieure ; la version actuelle est 4.6.</span><span class="sxs-lookup"><span data-stu-id="531a8-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="531a8-159">Les types d’application dans le volet central, choisissez **Ajouter dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="531a8-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="531a8-160">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="531a8-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="531a8-161">Également dans la section inférieure, cochez la case de **créer le répertoire pour la solution** .</span><span class="sxs-lookup"><span data-stu-id="531a8-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="531a8-162">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="531a8-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="531a8-163">L’Assistant Visual Studio demande quelques questions de suivi sur le site de paramètres Project Online (appelé SharePoint paramètres dans les boîtes de dialogue) dans les deux boîtes de dialogue qui suivent.</span><span class="sxs-lookup"><span data-stu-id="531a8-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="531a8-164">Voici les questions :</span><span class="sxs-lookup"><span data-stu-id="531a8-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="531a8-165">Quel site SharePoint que vous souhaitez utiliser pour le débogage de votre complément ?</span><span class="sxs-lookup"><span data-stu-id="531a8-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="531a8-166">Spécifier l’URL de votre site PWA, tel que https://contoso.sharepoint.com/sites/pwa.</span><span class="sxs-lookup"><span data-stu-id="531a8-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="531a8-167">Comment voulez-vous héberger votre Add-in SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="531a8-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="531a8-168">Sélectionnez [X] **hébergée par SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="531a8-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="531a8-169">Pour plus d’informations sur les compléments SharePoint, y compris les options d’hébergement, voir [SharePoint Add-ins](https://docs.microsoft.com/fr-fr/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="531a8-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/fr-fr/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="531a8-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="531a8-170">Click **Next**.</span></span> 
    
<span data-ttu-id="531a8-171">La seconde boîte de dialogue supplémentaire vous invite à spécifier la version de SharePoint Online pour le complément :</span><span class="sxs-lookup"><span data-stu-id="531a8-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="531a8-172">Qu’est la version la plus ancienne de SharePoint que vous souhaitez votre complément à cibler ?</span><span class="sxs-lookup"><span data-stu-id="531a8-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="531a8-173">Sélectionnez [X] S **HarePoint-en ligne**.</span><span class="sxs-lookup"><span data-stu-id="531a8-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="531a8-174">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="531a8-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="531a8-175">Visual Studio crée le projet et accède au site de projet en ligne.</span><span class="sxs-lookup"><span data-stu-id="531a8-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="531a8-176">Activer le chargement de version test sur le site Project Online</span><span class="sxs-lookup"><span data-stu-id="531a8-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="531a8-177">Chargement de version test est le mécanisme pour tester et déboguer des compléments Project Online. Deux scripts sont nécessaires pour le chargement de version test : un pour activer le chargement de version test sur votre site Project Online et un autre pour désactiver le chargement de version test une fois que vous avez terminé de tester et déboguer l’application add-in.</span><span class="sxs-lookup"><span data-stu-id="531a8-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="531a8-178">Pour plus d’informations sur la configuration de chargement de version test, voir [Activer l’application de chargement de version test dans votre collection de sites non-développeurs](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span><span class="sxs-lookup"><span data-stu-id="531a8-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="531a8-179">Applications de chargement de version test est une fonctionnalité de développement/test.</span><span class="sxs-lookup"><span data-stu-id="531a8-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="531a8-180">Il est **pas destiné à l’utilisation de production**.</span><span class="sxs-lookup"><span data-stu-id="531a8-180">It is **not intended for production use**.</span></span> <span data-ttu-id="531a8-181">Ne pas sideload applications régulièrement, ou conservez le chargement de version test application activée pendant plus de vous sont activement à l’aide de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="531a8-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="531a8-182">Ajouter du contenu dans le projet de complément</span><span class="sxs-lookup"><span data-stu-id="531a8-182">Add content to the add-in project</span></span>

<span data-ttu-id="531a8-183">Après avoir créé un projet et configurer le mécanisme de débogage, l’ajout de contenu à l’application comprend les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="531a8-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="531a8-184">Définition de l’étendue d’application</span><span class="sxs-lookup"><span data-stu-id="531a8-184">Setting the application scope</span></span>
    
- <span data-ttu-id="531a8-185">Liaison de la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="531a8-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="531a8-186">Ajout d’éléments d’interface utilisateur pour le complément</span><span class="sxs-lookup"><span data-stu-id="531a8-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="531a8-187">L’initialisation et connexion au service Project Online</span><span class="sxs-lookup"><span data-stu-id="531a8-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="531a8-188">Récupération des projets et les propriétés des détails</span><span class="sxs-lookup"><span data-stu-id="531a8-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="531a8-189">Affichage de projets</span><span class="sxs-lookup"><span data-stu-id="531a8-189">Displaying projects</span></span>
    
- <span data-ttu-id="531a8-190">Affichage des tâches pour un projet</span><span class="sxs-lookup"><span data-stu-id="531a8-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="531a8-191">Le projet de complément se compose de plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="531a8-191">The add-in project consists of many files.</span></span> <span data-ttu-id="531a8-192">Dans cet exemple, vous devrez modifier les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="531a8-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="531a8-193">Fichier AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="531a8-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="531a8-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="531a8-194">Default.aspx</span></span>
    
- <span data-ttu-id="531a8-195">App.js</span><span class="sxs-lookup"><span data-stu-id="531a8-195">App.js</span></span>
    
- <span data-ttu-id="531a8-196">App.CSS - facultatif ; contient des définitions de style développées pour le complément</span><span class="sxs-lookup"><span data-stu-id="531a8-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="531a8-197">Si le client Project Online change, telles que le déplacement d’une version d’évaluation vers un site d’abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion au serveur et l’URL du Site, à l’aide de la fenêtre Propriétés disponibles par le biais de l' **affichage** > **Propriétés Fenêtre** commande.</span><span class="sxs-lookup"><span data-stu-id="531a8-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="531a8-198">Vous pouvez également ajouter des fichiers au projet.</span><span class="sxs-lookup"><span data-stu-id="531a8-198">You can also add files to the project.</span></span> <span data-ttu-id="531a8-199">Dans ce cas, vous devrez mettre à jour le fichier Elements.xml situé dans le même groupe (contenu, Images, Pages ou Scripts) pour inclure les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="531a8-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="531a8-200">Pour plus d’informations sur les fichiers de projet, voir [Explorer la structure de manifeste d’application et le package d’un complément SharePoint](https://msdn.microsoft.com/fr-fr/library/office/fp179918.aspx.aspx).</span><span class="sxs-lookup"><span data-stu-id="531a8-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://msdn.microsoft.com/fr-fr/library/office/fp179918.aspx.aspx).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="531a8-201">Étendue d’application Set</span><span class="sxs-lookup"><span data-stu-id="531a8-201">Set application scope</span></span>

<span data-ttu-id="531a8-202">Le complément a besoin de niveaux de portée ou d’autorisation définis avant le service retourne des informations dans les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="531a8-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="531a8-203">Pour ce complément, utilisez l’étendue suivante au projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="531a8-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="531a8-204">Cette modification est apportée au fichier AppManifest.xml dans l’onglet autorisations :</span><span class="sxs-lookup"><span data-stu-id="531a8-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="531a8-205">Domaine d’application</span><span class="sxs-lookup"><span data-stu-id="531a8-205">Scope</span></span>|<span data-ttu-id="531a8-206">Autorisation</span><span class="sxs-lookup"><span data-stu-id="531a8-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="531a8-207">Plusieurs projets (Project Server)</span><span class="sxs-lookup"><span data-stu-id="531a8-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="531a8-208">Lire</span><span class="sxs-lookup"><span data-stu-id="531a8-208">Read</span></span>  <br/> |
   
<span data-ttu-id="531a8-209">Enregistrez le fichier après la définition de l’étendue de l’application.</span><span class="sxs-lookup"><span data-stu-id="531a8-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="531a8-210">Dans le cas contraire, aucune donnée n’est renvoyées depuis le service.</span><span class="sxs-lookup"><span data-stu-id="531a8-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="531a8-211">Lier la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="531a8-211">Link the JSOM library</span></span>

<span data-ttu-id="531a8-212">Les bibliothèques de Project Online runtime, PS.js et PS.debug.js, sont fournis par Project Online et sont toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="531a8-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="531a8-213">Compléments JavaScript qui utilisent le JSOM doivent être liée à une de ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="531a8-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="531a8-214">Les définitions de liaison sont ajoutées dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="531a8-215">Les commandes à utiliser le PS.js et/ou PS.debug.js font partie du code situé dans le fichier App.js.</span><span class="sxs-lookup"><span data-stu-id="531a8-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="531a8-216">Ajoutez la commande suivante pour la définition de PS.js ou PS.debug.js dans les `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` élément suivant « SharePoint:ScriptLink » pour sp.js.</span><span class="sxs-lookup"><span data-stu-id="531a8-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="531a8-217">L’attribut **à la demande** pour PS.js ou PS.debug.js défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="531a8-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="531a8-218">Ajouter des éléments d’interface utilisateur pour le complément</span><span class="sxs-lookup"><span data-stu-id="531a8-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="531a8-219">L’exemple complément se compose de certains composants.</span><span class="sxs-lookup"><span data-stu-id="531a8-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="531a8-220">Description des éléments statiques se trouvent dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="531a8-221">Descriptions des éléments dynamiques et code pour tous les composants se trouvent dans le fichier App.js.</span><span class="sxs-lookup"><span data-stu-id="531a8-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="531a8-222">Pour les commentaires concernant les composants, consultez les exemples de code source.</span><span class="sxs-lookup"><span data-stu-id="531a8-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="531a8-223">Voici une liste des composants de l’interface utilisateur dans le complément :</span><span class="sxs-lookup"><span data-stu-id="531a8-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="531a8-224">Titre</span><span class="sxs-lookup"><span data-stu-id="531a8-224">Title</span></span>
    
- <span data-ttu-id="531a8-225">Formulation de présentation</span><span class="sxs-lookup"><span data-stu-id="531a8-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="531a8-226">Pour supprimer des tâches à partir de la table</span><span class="sxs-lookup"><span data-stu-id="531a8-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="531a8-227">Tableau qui répertorie les informations sur la tâche et nom et l’ID du projet.</span><span class="sxs-lookup"><span data-stu-id="531a8-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="531a8-228">Bouton (cloné en une seule fois pour chaque projet) qui importe les données de tâche dans le tableau des tâches.</span><span class="sxs-lookup"><span data-stu-id="531a8-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="531a8-229">Pour plus d’informations de l’interface utilisateur, telles que le titre et l’en-tête de la table de projet, consultez le fichier de projet Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="531a8-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="531a8-230">Initialiser et se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="531a8-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="531a8-231">Le fichier App.js contient le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="531a8-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="531a8-232">Le complément PS.js est chargé dans le navigateur, puis appelle la fonction initializePage.</span><span class="sxs-lookup"><span data-stu-id="531a8-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="531a8-233">InitializePage récupère un contexte au point de terminaison Project Online et démarre la fonction loadProjects.</span><span class="sxs-lookup"><span data-stu-id="531a8-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a><span data-ttu-id="531a8-234">Récupérer les projets</span><span class="sxs-lookup"><span data-stu-id="531a8-234">Retrieve the projects</span></span>

<span data-ttu-id="531a8-235">La fonction loadProjects demande au service de l’ID et noms de projets.</span><span class="sxs-lookup"><span data-stu-id="531a8-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="531a8-236">L’application extrait le nom du projet et le projet de code. Autres informations sur le projet est disponibles et est accessible en modifiant la méthode load pour identifier explicitement les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="531a8-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="531a8-237">Un exemple est fourni dans le code comme un commentaire.</span><span class="sxs-lookup"><span data-stu-id="531a8-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="531a8-238">Si la requête aboutit, le complément se poursuit en appelant displayProjects.</span><span class="sxs-lookup"><span data-stu-id="531a8-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a><span data-ttu-id="531a8-239">Afficher les projets</span><span class="sxs-lookup"><span data-stu-id="531a8-239">Display the projects</span></span>

<span data-ttu-id="531a8-240">La fonction displayProjects crée une table, une ligne par projet et un bouton pour afficher les tâches du projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="531a8-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="531a8-241">La boucle while accède à l’ID et des propriétés de nom.</span><span class="sxs-lookup"><span data-stu-id="531a8-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="531a8-242">Il s’agit légèrement différent de celui du projet de code source qui appelle une fonction qui, à son tour, accède aux propriétés de la même.</span><span class="sxs-lookup"><span data-stu-id="531a8-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="531a8-243">Afficher les tâches pour un projet</span><span class="sxs-lookup"><span data-stu-id="531a8-243">Display the tasks for a project</span></span>

<span data-ttu-id="531a8-244">Les tâches, lors de la partie de la macro complémentaire, ne font pas partie du chargement initial.</span><span class="sxs-lookup"><span data-stu-id="531a8-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="531a8-245">Si l’utilisateur est intéressée par les tâches associées à un projet, cliquez sur le bouton « Afficher les tâches » entraîne les tâches à afficher dans la liste en utilisant le Gestionnaire d’événements btnLoadTasks.</span><span class="sxs-lookup"><span data-stu-id="531a8-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="531a8-246">Le Gestionnaire d’événements btnLoadTasks, avec l’ID de projet approprié, demande les tâches pour le projet spécifié à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="531a8-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="531a8-247">Une fois récupéré, btnLoadTasks transmet la liste des tâches à displayTasks pour présenter les tâches à l’écran.</span><span class="sxs-lookup"><span data-stu-id="531a8-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

<span data-ttu-id="531a8-248">La fonction displayTasks affiche les tâches associées à un projet spécifié immédiatement après l’écriture du projet.</span><span class="sxs-lookup"><span data-stu-id="531a8-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="531a8-249">La boucle while accède à l’ID de tâche et les propriétés de nom.</span><span class="sxs-lookup"><span data-stu-id="531a8-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="531a8-250">Il s’agit légèrement différent de celui du projet de code source qui appelle une fonction qui, à son tour, accède aux propriétés de la même.</span><span class="sxs-lookup"><span data-stu-id="531a8-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="531a8-251">Exemple de sortie pour les tâches d’un projet unique suit.</span><span class="sxs-lookup"><span data-stu-id="531a8-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="531a8-252">![Capture d’écran montrant la sortie d’une tâche de projet] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Capture d’écran montrant la sortie d’une tâche de projet")</span><span class="sxs-lookup"><span data-stu-id="531a8-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="531a8-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="531a8-253">See also</span></span>

<span data-ttu-id="531a8-254">Pour la documentation et des exemples relatifs à Project Online et développement d’applications à l’aide de CSOM, voir le [Portail de développement Project](http://dev.office.com/project.aspx).</span><span class="sxs-lookup"><span data-stu-id="531a8-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    

