---
title: Développement d'un complément Project Online à l'aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit le développement de compléments Microsoft Project Online pour améliorer votre expérience avec Project online. Le projet de développement est implémenté en tant que procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d'explorer les tâches associées à des projets individuels.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322685"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="8d04c-105">Développement d'un complément Project Online à l'aide du modèle objet JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="8d04c-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="8d04c-106">Cet article décrit le développement de compléments Microsoft Project Online pour améliorer votre expérience avec le Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="8d04c-107">Le projet de développement est implémenté en tant que procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="8d04c-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="8d04c-108">Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d'explorer les tâches associées à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="8d04c-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="8d04c-109">Au moment de l'exécution, la liste de compléments se présente comme dans l'illustration suivante:</span><span class="sxs-lookup"><span data-stu-id="8d04c-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="8d04c-110">![Capture d'écran illustrant une liste de tâches et de projets JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Capture d'écran illustrant une liste de tâches et de projets JSOM")</span><span class="sxs-lookup"><span data-stu-id="8d04c-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="8d04c-111">L'objectif de l'exemple est l'interaction avec le projet Online, la création de requêtes et la définition du contexte pour chaque demande du service.</span><span class="sxs-lookup"><span data-stu-id="8d04c-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="8d04c-112">Les éléments de l'interface utilisateur (IU) reçoivent peu d'attention.</span><span class="sxs-lookup"><span data-stu-id="8d04c-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="8d04c-113">Au lieu de cela, les listes sources fournissent des commentaires sur l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d04c-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d04c-114">Les fichiers sources de l'exemple de complément, un projet Visual Studio, sont disponibles à l'adresse https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....suivante:.</span><span class="sxs-lookup"><span data-stu-id="8d04c-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="8d04c-115">Conservez les fichiers sources comme référence pendant que vous lisez l'article, car chacun complète l'autre.</span><span class="sxs-lookup"><span data-stu-id="8d04c-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="8d04c-116">Les fichiers dans Visual Studio Project Build et sont exécutables avec un minimum de modifications — en substituant l'URL de votre client Project Online au dossier PWA.</span><span class="sxs-lookup"><span data-stu-id="8d04c-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="8d04c-117">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="8d04c-117">Background</span></span>

<span data-ttu-id="8d04c-118">Project Online est un service Office 365 qui offre aux entreprises une solution de gestion de portefeuille de projets (PPM) et de gestion de projets (PMO) pour coordonner et gérer les portefeuilles, les programmes et les projets.</span><span class="sxs-lookup"><span data-stu-id="8d04c-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="8d04c-119">Project Online est une offre différente de celle des éditions de bureau de Project. Cependant, Project Online contient toujours la fonctionnalité permettant de maintenir et de suivre les détails du projet tout au long de la vie d'un projet.</span><span class="sxs-lookup"><span data-stu-id="8d04c-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="8d04c-120">Project Online est basé sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="8d04c-121">Un complément hébergé sur Project Online est composé de fichiers JavaScript et de fichiers de ressources qui interagissent avec l'API de modèle objet côté client.</span><span class="sxs-lookup"><span data-stu-id="8d04c-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="8d04c-122">Lorsque l'utilisateur visite le complément, le JavaScript et les ressources sont téléchargés et exécutés dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="8d04c-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="8d04c-123">Le complément effectue des appels asynchrones à Project Online pour interagir avec le service, qu'il s'agisse de créer, de récupérer, de mettre à jour ou de supprimer des données.</span><span class="sxs-lookup"><span data-stu-id="8d04c-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="8d04c-124">Project Online effectue une action supplémentaire pour protéger les informations qui appartiennent à d'autres clients du complément; en d'autres termes, Project Online crée un site isolé pour interagir avec les demandes du complément.</span><span class="sxs-lookup"><span data-stu-id="8d04c-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="8d04c-125">Aucun code personnalisé n'est exécuté sur l'hôte Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="8d04c-126">Le programme d'installation du développement pour les compléments Project Online utilise le type de projet complément Visual Studio SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d04c-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="8d04c-127">Le complément est écrit en JavaScript et utilise le modèle objet JavaScript (JSOM) Project pour interagir avec le service Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="8d04c-128">Le JSOM hérite de la plupart de ses fonctionnalités du JSOM SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d04c-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d04c-129">Les compléments peuvent être publiés et vendus dans l'Office Store ou déployés sur un catalogue d'applications privé sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d04c-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="8d04c-130">Pour plus d'informations, consultez [la rubrique deploy and Publish Your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span><span class="sxs-lookup"><span data-stu-id="8d04c-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="8d04c-131">Le complément utilisé dans cet article est un exemple pour les développeurs; Il n'est pas destiné à être utilisé dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="8d04c-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="8d04c-132">L'objectif principal est de présenter un exemple de développement d'applications pour Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="8d04c-133">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="8d04c-133">Prerequisites</span></span>

<span data-ttu-id="8d04c-134">Ajoutez les éléments suivants à un environnement Windows pris en charge:</span><span class="sxs-lookup"><span data-stu-id="8d04c-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="8d04c-135">**.NET Framework 4,0 ou version ultérieure**: les versions complètes de l'infrastructure à partir de la version 4,0 sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="8d04c-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="8d04c-136">Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="8d04c-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="8d04c-137">**Visual Studio 2013 ou version ultérieure**:</span><span class="sxs-lookup"><span data-stu-id="8d04c-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="8d04c-138">L'édition Professional de Visual Studio 2015 est prête à être prête à l'emploi et est disponible sur le site https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="8d04c-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="8d04c-139">L'édition communautaire de Visual Studio 2015 est disponible à https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspxl'adresse.</span><span class="sxs-lookup"><span data-stu-id="8d04c-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="8d04c-140">Cette édition nécessite l'installation manuelle des outils de développement Microsoft Office pour Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8d04c-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="8d04c-141">Les outils de développement Microsoft Office pour Visual Studio sont disponibles https://www.visualstudio.com/en-us/features/office-tools-vs.aspxsur le site.</span><span class="sxs-lookup"><span data-stu-id="8d04c-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="8d04c-142">**Un compte Project Online**: cela permet d'accéder au service d'hébergement.</span><span class="sxs-lookup"><span data-stu-id="8d04c-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="8d04c-143">Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="8d04c-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="8d04c-144">Assurez-vous que l'utilisateur du complément dispose d'une autorisation suffisante pour accéder à certains projets dans le client Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="8d04c-145">**Projets sur le site d'hébergement** qui sont renseignés avec les informations.</span><span class="sxs-lookup"><span data-stu-id="8d04c-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8d04c-146">Le .NET Framework standard est l'infrastructure appropriée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8d04c-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="8d04c-147">N'utilisez pas le «.NET Framework 4 Client Profile».</span><span class="sxs-lookup"><span data-stu-id="8d04c-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="8d04c-148">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8d04c-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="8d04c-149">La configuration de l'application consiste à créer un nouveau projet, à lier les bibliothèques appropriées et à déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8d04c-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="8d04c-150">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="8d04c-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="8d04c-151">La section est brève et très simple.</span><span class="sxs-lookup"><span data-stu-id="8d04c-151">The section is brief and very basic.</span></span> <span data-ttu-id="8d04c-152">La valeur est que les informations sont fusionnées à un seul endroit.</span><span class="sxs-lookup"><span data-stu-id="8d04c-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="8d04c-153">Sélectionner un projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8d04c-153">Select a Visual Studio project</span></span>

<span data-ttu-id="8d04c-154">Pour créer un projet du type approprié pour le complément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8d04c-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="8d04c-155">Les mots clés rencontrés à l'écran ont un attribut **Bold** :</span><span class="sxs-lookup"><span data-stu-id="8d04c-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="8d04c-156">Dans le menu fichier, choisissez **fichier** > **nouveau** > **projet**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="8d04c-157">Dans les modèles installés dans le volet gauche, sélectionnez**compléments Web** **C#** > **Office/SharePoint** > .</span><span class="sxs-lookup"><span data-stu-id="8d04c-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="8d04c-158">En haut du volet central, sélectionnez **.NET Framework 4** ou version ultérieure; la version actuelle est 4,6.</span><span class="sxs-lookup"><span data-stu-id="8d04c-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="8d04c-159">Dans les types d'applications du volet central, choisissez **complément SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="8d04c-160">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="8d04c-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="8d04c-161">Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="8d04c-162">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="8d04c-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="8d04c-163">L'Assistant Visual Studio pose quelques questions de suivi sur le site des paramètres de Project Online (appelés paramètres SharePoint dans les boîtes de dialogue) en deux boîtes de dialogue qui suivent.</span><span class="sxs-lookup"><span data-stu-id="8d04c-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="8d04c-164">Voici les questions:</span><span class="sxs-lookup"><span data-stu-id="8d04c-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="8d04c-165">Quel site SharePoint souhaitez-vous utiliser pour le débogage de votre complément?</span><span class="sxs-lookup"><span data-stu-id="8d04c-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="8d04c-166">Spécifiez l'URL de votre site PWA, par https://contoso.sharepoint.com/sites/pwaexemple.</span><span class="sxs-lookup"><span data-stu-id="8d04c-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="8d04c-167">Comment souhaitez-vous héberger votre complément SharePoint?</span><span class="sxs-lookup"><span data-stu-id="8d04c-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="8d04c-168">Choisissez [X] **hébergement par SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="8d04c-169">Pour plus d'informations sur les compléments SharePoint, y compris les options d'hébergement, voir compléments pour [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="8d04c-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="8d04c-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-170">Click **Next**.</span></span> 
    
<span data-ttu-id="8d04c-171">La deuxième boîte de dialogue supplémentaire vous demande de spécifier la version SharePoint Online pour le complément:</span><span class="sxs-lookup"><span data-stu-id="8d04c-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="8d04c-172">Quelle est la version la plus récente de SharePoint que vous souhaitez que votre complément cible?</span><span class="sxs-lookup"><span data-stu-id="8d04c-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="8d04c-173">Choisissez [X] S **harePoint-Online**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="8d04c-174">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="8d04c-175">Visual Studio crée le projet et accède au site Project online.</span><span class="sxs-lookup"><span data-stu-id="8d04c-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="8d04c-176">Activer chargement sur le site Project Online</span><span class="sxs-lookup"><span data-stu-id="8d04c-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="8d04c-177">Chargement est le mécanisme de test et de débogage des compléments Project online. Vous avez besoin de deux scripts pour chargement: un pour activer chargement sur votre site Project Online et un autre pour désactiver chargement une fois que vous avez terminé de tester et de déboguer le complément.</span><span class="sxs-lookup"><span data-stu-id="8d04c-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="8d04c-178">Pour plus d'informations sur la configuration de chargement, consultez [la rubrique activation de l'application chargement dans votre collection de sites autres que les développeurs](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span><span class="sxs-lookup"><span data-stu-id="8d04c-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d04c-179">Les applications chargement sont une fonctionnalité de développeur/test.</span><span class="sxs-lookup"><span data-stu-id="8d04c-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="8d04c-180">Il n'est **pas destiné à une utilisation de production**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-180">It is **not intended for production use**.</span></span> <span data-ttu-id="8d04c-181">Ne pas chargement les applications régulièrement ou conserver l'application chargement activée plus longtemps que vous n'utilisez activement cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8d04c-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="8d04c-182">Ajouter du contenu au projet de complément</span><span class="sxs-lookup"><span data-stu-id="8d04c-182">Add content to the add-in project</span></span>

<span data-ttu-id="8d04c-183">Après avoir créé un projet et configuré le mécanisme de débogage, l'ajout de contenu à l'application inclut les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="8d04c-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="8d04c-184">Définition de l'étendue de l'application</span><span class="sxs-lookup"><span data-stu-id="8d04c-184">Setting the application scope</span></span>
    
- <span data-ttu-id="8d04c-185">Liaison de la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="8d04c-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="8d04c-186">Ajout d'éléments d'interface utilisateur au complément</span><span class="sxs-lookup"><span data-stu-id="8d04c-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="8d04c-187">Initialisation et connexion au service Project Online</span><span class="sxs-lookup"><span data-stu-id="8d04c-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="8d04c-188">Récupération de projets et de détails/propriétés</span><span class="sxs-lookup"><span data-stu-id="8d04c-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="8d04c-189">Affichage de projets</span><span class="sxs-lookup"><span data-stu-id="8d04c-189">Displaying projects</span></span>
    
- <span data-ttu-id="8d04c-190">Affichage des tâches pour un projet</span><span class="sxs-lookup"><span data-stu-id="8d04c-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="8d04c-191">Le projet de complément est composé de nombreux fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d04c-191">The add-in project consists of many files.</span></span> <span data-ttu-id="8d04c-192">Dans cet exemple, vous devez modifier les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="8d04c-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="8d04c-193">AppManifest. Xml</span><span class="sxs-lookup"><span data-stu-id="8d04c-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="8d04c-194">Default. aspx</span><span class="sxs-lookup"><span data-stu-id="8d04c-194">Default.aspx</span></span>
    
- <span data-ttu-id="8d04c-195">App. js</span><span class="sxs-lookup"><span data-stu-id="8d04c-195">App.js</span></span>
    
- <span data-ttu-id="8d04c-196">App. CSS: facultatif; contient les définitions de style développées pour le complément.</span><span class="sxs-lookup"><span data-stu-id="8d04c-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="8d04c-197">Si le client Project Online change, par exemple lors du passage d'une version d'évaluation à un site d'abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion au serveur et l'URL du site, à l'aide de la fenêtre Propriétés disponible via les propriétés d' **affichage** > .\*\* Commande fenêtre\*\* .</span><span class="sxs-lookup"><span data-stu-id="8d04c-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="8d04c-198">Vous pouvez également ajouter des fichiers au projet.</span><span class="sxs-lookup"><span data-stu-id="8d04c-198">You can also add files to the project.</span></span> <span data-ttu-id="8d04c-199">Si c'est le cas, vous devez mettre à jour le fichier Elements. xml situé dans le même groupe (contenu, images, pages ou scripts) afin d'inclure les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d04c-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="8d04c-200">Pour plus d'informations sur les fichiers de projet, voir [Explorer la structure du manifeste de l'application et le package d'un complément SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span><span class="sxs-lookup"><span data-stu-id="8d04c-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="8d04c-201">Définir l'étendue de l'application</span><span class="sxs-lookup"><span data-stu-id="8d04c-201">Set application scope</span></span>

<span data-ttu-id="8d04c-202">Le complément a besoin d'une étendue ou de niveaux d'autorisation définis avant que le service renvoie des informations dans les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="8d04c-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="8d04c-203">Pour ce complément, utilisez l'étendue suivante pour le projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8d04c-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="8d04c-204">Cette modification est apportée au fichier AppManifest. xml dans l'onglet Autorisations:</span><span class="sxs-lookup"><span data-stu-id="8d04c-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="8d04c-205">Portée</span><span class="sxs-lookup"><span data-stu-id="8d04c-205">Scope</span></span>|<span data-ttu-id="8d04c-206">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8d04c-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d04c-207">Projets multiples (Project Server)</span><span class="sxs-lookup"><span data-stu-id="8d04c-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="8d04c-208">Lecture</span><span class="sxs-lookup"><span data-stu-id="8d04c-208">Read</span></span>  <br/> |
   
<span data-ttu-id="8d04c-209">Enregistrez le fichier après avoir défini l'étendue de l'application.</span><span class="sxs-lookup"><span data-stu-id="8d04c-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="8d04c-210">Dans le cas contraire, aucune donnée ne sera renvoyée par le service.</span><span class="sxs-lookup"><span data-stu-id="8d04c-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="8d04c-211">Liaison de la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="8d04c-211">Link the JSOM library</span></span>

<span data-ttu-id="8d04c-212">Les bibliothèques Project Online de l'exécution, PS. js et PS. Debug. js, sont fournies par Project Online et sont toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="8d04c-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="8d04c-213">Les compléments JavaScript qui utilisent JSOM doivent être liés à l'une de ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="8d04c-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="8d04c-214">Les définitions de liaison sont ajoutées au fichier default. aspx.</span><span class="sxs-lookup"><span data-stu-id="8d04c-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="8d04c-215">Les commandes permettant d'utiliser PS. js et/ou PS. Debug. js font partie du code se trouvant dans le fichier app. js.</span><span class="sxs-lookup"><span data-stu-id="8d04c-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="8d04c-216">Ajoutez la commande suivante pour la définition PS. js ou PS. Debug. js dans `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` l'élément suivant le «SharePoint: ScriptLink» pour SP. js.</span><span class="sxs-lookup"><span data-stu-id="8d04c-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="8d04c-217">L'attribut **OnDemand** pour PS. js ou PS. Debug. js a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="8d04c-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="8d04c-218">Ajouter des éléments d'interface utilisateur au complément</span><span class="sxs-lookup"><span data-stu-id="8d04c-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="8d04c-219">L'exemple de complément se compose de quelques composants.</span><span class="sxs-lookup"><span data-stu-id="8d04c-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="8d04c-220">Les descriptions des éléments statiques se trouvent dans le fichier default. aspx.</span><span class="sxs-lookup"><span data-stu-id="8d04c-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="8d04c-221">Les descriptions et le code des éléments dynamiques de tous les composants se trouvent dans le fichier app. js.</span><span class="sxs-lookup"><span data-stu-id="8d04c-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="8d04c-222">Pour les commentaires relatifs aux composants, reportez-vous aux listes de codes source.</span><span class="sxs-lookup"><span data-stu-id="8d04c-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="8d04c-223">Voici une liste des composants de l'interface utilisateur dans le complément:</span><span class="sxs-lookup"><span data-stu-id="8d04c-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="8d04c-224">Titre</span><span class="sxs-lookup"><span data-stu-id="8d04c-224">Title</span></span>
    
- <span data-ttu-id="8d04c-225">Formulation de présentation</span><span class="sxs-lookup"><span data-stu-id="8d04c-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="8d04c-226">Bouton permettant de supprimer des tâches du tableau</span><span class="sxs-lookup"><span data-stu-id="8d04c-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="8d04c-227">Tableau répertoriant l'ID et le nom du projet, ainsi que les informations sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="8d04c-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="8d04c-228">Bouton tâches (cloné une fois pour chaque projet) qui importe des données de tâches dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8d04c-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="8d04c-229">Pour plus d'informations sur l'interface utilisateur, telles que le titre et la partie d'en-tête de la table Project, voir le fichier de projet default. aspx.</span><span class="sxs-lookup"><span data-stu-id="8d04c-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="8d04c-230">Initialiser et se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="8d04c-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="8d04c-231">Le fichier app. js contient le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8d04c-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="8d04c-232">Le complément charge PS. js dans le navigateur, puis appelle la fonction initializePage.</span><span class="sxs-lookup"><span data-stu-id="8d04c-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="8d04c-233">InitializePage récupère un contexte pour le point de terminaison Project Online et démarre la fonction loadProjects.</span><span class="sxs-lookup"><span data-stu-id="8d04c-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="8d04c-234">Récupérer les projets</span><span class="sxs-lookup"><span data-stu-id="8d04c-234">Retrieve the projects</span></span>

<span data-ttu-id="8d04c-235">La fonction loadProjects interroge le service pour les noms de projet et les ID.</span><span class="sxs-lookup"><span data-stu-id="8d04c-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="8d04c-236">L'application récupère le nom du projet et l'ID du projet. D'autres informations sur le projet sont disponibles et peuvent être consultées en modifiant la méthode Load pour identifier explicitement les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="8d04c-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="8d04c-237">Un exemple est fourni dans le code sous forme de commentaire.</span><span class="sxs-lookup"><span data-stu-id="8d04c-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="8d04c-238">Si la requête réussit, le complément continue en appelant displayProjects.</span><span class="sxs-lookup"><span data-stu-id="8d04c-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="8d04c-239">Afficher les projets</span><span class="sxs-lookup"><span data-stu-id="8d04c-239">Display the projects</span></span>

<span data-ttu-id="8d04c-240">La fonction displayProjects crée un tableau, une ligne par projet et un bouton pour afficher les tâches du projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="8d04c-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="8d04c-241">La boucle while accède aux propriétés ID et Name.</span><span class="sxs-lookup"><span data-stu-id="8d04c-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="8d04c-242">Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés.</span><span class="sxs-lookup"><span data-stu-id="8d04c-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="8d04c-243">Afficher les tâches d'un projet</span><span class="sxs-lookup"><span data-stu-id="8d04c-243">Display the tasks for a project</span></span>

<span data-ttu-id="8d04c-244">Les tâches, dans le cadre du complément, ne font pas partie du chargement initial.</span><span class="sxs-lookup"><span data-stu-id="8d04c-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="8d04c-245">Si l'utilisateur est intéressé par les tâches associées à un projet, le fait de cliquer sur le bouton «afficher les tâches» entraîne l'affichage des tâches dans la liste à l'aide du gestionnaire d'événements btnLoadTasks.</span><span class="sxs-lookup"><span data-stu-id="8d04c-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="8d04c-246">Le gestionnaire d'événements btnLoadTasks, avec l'ID de projet approprié, demande les tâches pour le projet spécifié sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="8d04c-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="8d04c-247">Une fois récupéré, btnLoadTasks transmet la liste de tâches à displayTasks pour présenter les tâches affichées à l'écran.</span><span class="sxs-lookup"><span data-stu-id="8d04c-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="8d04c-248">La fonction displayTasks affiche les tâches associées à un projet spécifié immédiatement au-dessous de l'entrée de projet.</span><span class="sxs-lookup"><span data-stu-id="8d04c-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="8d04c-249">La boucle while accède aux propriétés ID et nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="8d04c-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="8d04c-250">Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés.</span><span class="sxs-lookup"><span data-stu-id="8d04c-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="8d04c-251">Un exemple de sortie pour les tâches d'un projet unique suit.</span><span class="sxs-lookup"><span data-stu-id="8d04c-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="8d04c-252">![Capture d'écran illustrant la sortie d'une tâche de projet] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Capture d'écran illustrant la sortie d'une tâche de projet")</span><span class="sxs-lookup"><span data-stu-id="8d04c-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d04c-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d04c-253">See also</span></span>

<span data-ttu-id="8d04c-254">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="8d04c-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


