---
title: Développement d’un add-in Project Online à l’aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit le développement d’un add-in Microsoft Project Online pour améliorer votre expérience avec Project Online. Le projet de développement est implémenté comme une walkthrough. Le add-in utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’extraire les tâches associées à des projets individuels.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322685"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="14893-105">Développement d’un add-in Project Online à l’aide du modèle objet JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="14893-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="14893-106">Cet article décrit le développement d’un add-in Microsoft Project Online pour améliorer votre expérience avec Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="14893-107">Le projet de développement est implémenté comme une walkthrough.</span><span class="sxs-lookup"><span data-stu-id="14893-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="14893-108">Le add-in utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’extraire les tâches associées à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="14893-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="14893-109">Au moment de l’exécuter, la liste des modules de recherche ressemble à l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="14893-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="14893-110">![Capture d’écran montrant une liste de projets et]de tâches JSOM Capture d’écran montrant une liste de projets et de tâches(media/766e5914-f048-48f4-9282-291f55e6e90d.png "JSOM")</span><span class="sxs-lookup"><span data-stu-id="14893-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="14893-111">L’objectif de l’exemple est l’interaction avec Project Online, l’établissement de requêtes et la définition du contexte pour chaque demande du service.</span><span class="sxs-lookup"><span data-stu-id="14893-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="14893-112">Les éléments d’interface utilisateur reçoivent une attention minimale.</span><span class="sxs-lookup"><span data-stu-id="14893-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="14893-113">Au lieu de cela, les listes sources fournissent des commentaires concernant l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14893-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="14893-114">Les fichiers sources pour l’exemple de Visual Studio, sont disponibles à l’Visual Studio https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... :</span><span class="sxs-lookup"><span data-stu-id="14893-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="14893-115">Gardez les fichiers sources à portée de main en tant que référence pendant que vous lisez l’article, car chacun d’eux complète l’autre.</span><span class="sxs-lookup"><span data-stu-id="14893-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="14893-116">Les fichiers de la Visual Studio projet sont exécutables avec des modifications minimales, en remplaçant l’URL de votre client Project Online par le dossier PWA.</span><span class="sxs-lookup"><span data-stu-id="14893-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="14893-117">Contexte</span><span class="sxs-lookup"><span data-stu-id="14893-117">Background</span></span>

<span data-ttu-id="14893-118">Project Online est un service Office 365 qui fournit aux entreprises une solution de gestion de portefeuille de projets (PPM) et de bureau de gestion de projet (PMO) pour coordonner et gérer des portefeuilles, des programmes et des projets.</span><span class="sxs-lookup"><span data-stu-id="14893-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="14893-119">Project Online est une offre différente des éditions de bureau project ; Toutefois, Project Online contient toujours la fonctionnalité de maintenance et de suivi des détails d’un projet tout au long de la durée de vie d’un projet.</span><span class="sxs-lookup"><span data-stu-id="14893-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="14893-120">Project Online repose sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="14893-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="14893-121">Un add-in hébergé par Project Online se compose de fichiers JavaScript et de ressources qui interagissent avec l’API client-side-object-model.</span><span class="sxs-lookup"><span data-stu-id="14893-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="14893-122">Lorsque l’utilisateur visite le add-in, le JavaScript et les ressources sont téléchargés et exécutés dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="14893-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="14893-123">Le add-In effectue des appels asynchrones à Project Online pour interagir avec le service, que ce soit pour créer, récupérer, mettre à jour ou supprimer des données.</span><span class="sxs-lookup"><span data-stu-id="14893-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="14893-124">Project Online effectue une action de plus pour protéger les informations qui appartiennent à d’autres locataires du module complémentaire . c’est-à-dire, Project Online crée un site isolé pour interagir avec les demandes du module.</span><span class="sxs-lookup"><span data-stu-id="14893-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="14893-125">Aucun code personnalisé ne s’exécute sur l’hôte Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="14893-126">La configuration de développement pour les applications Project Online utilise le type Visual Studio projet de l’Add-in SharePoint.</span><span class="sxs-lookup"><span data-stu-id="14893-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="14893-127">Le add-in est écrit en JavaScript et utilise le modèle objet JavaScript project (JSOM) pour interagir avec le service Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="14893-128">Le JSOM hérite de la plupart de ses fonctionnalités du JSOM SharePoint.</span><span class="sxs-lookup"><span data-stu-id="14893-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="14893-129">Les applications peuvent être publiées et vendues dans l’Office Store ou déployées dans un catalogue d’applications privé sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="14893-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="14893-130">Pour plus d’informations, [voir Déployer et publier votre add-in Office.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)</span><span class="sxs-lookup"><span data-stu-id="14893-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="14893-131">Le add-in utilisé dans cet article est un exemple pour les développeurs . il n’est pas destiné à être utilisé dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="14893-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="14893-132">L’objectif principal est d’afficher un exemple de développement d’applications pour Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="14893-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14893-133">Prerequisites</span></span>

<span data-ttu-id="14893-134">Ajoutez les éléments suivants à un environnement Windows pris en charge :</span><span class="sxs-lookup"><span data-stu-id="14893-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="14893-135">**.NET Framework 4.0** ou version ultérieure : les versions complètes de l’infrastructure de la version 4.0 sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="14893-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="14893-136">Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="14893-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="14893-137">**Visual Studio 2013 ou ultérieure**:</span><span class="sxs-lookup"><span data-stu-id="14893-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="14893-138">L’édition professionnelle Visual Studio 2015 est prête à l’emploi et est disponible sur https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="14893-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="14893-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="14893-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="14893-140">Cette édition nécessite l’installation manuelle des outils Microsoft Office développeur pour Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="14893-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="14893-141">Les outils Microsoft Office développeur pour Visual Studio sont disponibles sur https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="14893-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="14893-142">**Un compte Project Online :** cela permet d’accéder au service d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="14893-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="14893-143">Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="14893-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="14893-144">Assurez-vous que l’utilisateur du add-in dispose d’une autorisation suffisante pour accéder à certains projets dans le client Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="14893-145">**Projets sur le site d’hébergement** qui sont remplis avec des informations.</span><span class="sxs-lookup"><span data-stu-id="14893-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="14893-146">Le .NET Framework standard est l’infrastructure correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="14893-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="14893-147">N’utilisez pas le « profil client .NET Framework 4 ».</span><span class="sxs-lookup"><span data-stu-id="14893-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="14893-148">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14893-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="14893-149">La configuration de l’application consiste à créer un projet, à lier les bibliothèques appropriées et à déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="14893-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="14893-150">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="14893-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="14893-151">La section est brève et très simple.</span><span class="sxs-lookup"><span data-stu-id="14893-151">The section is brief and very basic.</span></span> <span data-ttu-id="14893-152">La valeur est que les informations sont resserées à un seul endroit.</span><span class="sxs-lookup"><span data-stu-id="14893-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="14893-153">Sélectionner un projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14893-153">Select a Visual Studio project</span></span>

<span data-ttu-id="14893-154">Pour créer un projet du type approprié pour le module, vous devez suivre les étapes ci-après.</span><span class="sxs-lookup"><span data-stu-id="14893-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="14893-155">Les mots clés rencontrés à l’écran ont un **attribut gras** :</span><span class="sxs-lookup"><span data-stu-id="14893-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="14893-156">Dans le menu Fichier, choisissez **Fichier**  >  **nouveau**  >  **projet.**</span><span class="sxs-lookup"><span data-stu-id="14893-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="14893-157">Dans les modèles installés dans le volet gauche, sélectionnez **C#**  >  **Office/SharePoint**  >  **Web Add-ins**.</span><span class="sxs-lookup"><span data-stu-id="14893-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="14893-158">En haut du volet central, sélectionnez **.NET Framework 4 ou** ultérieur ; la version actuelle est 4.6.</span><span class="sxs-lookup"><span data-stu-id="14893-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="14893-159">À partir des types d’applications dans le volet central, sélectionnez **SharePoint Add-in**.</span><span class="sxs-lookup"><span data-stu-id="14893-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="14893-160">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="14893-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="14893-161">Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**.</span><span class="sxs-lookup"><span data-stu-id="14893-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="14893-162">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="14893-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="14893-163">L’Assistant Visual Studio pose quelques questions de suivi sur le site de paramètres Project Online (appelé paramètres SharePoint dans les boîtes de dialogue) dans quelques boîtes de dialogue qui suivent.</span><span class="sxs-lookup"><span data-stu-id="14893-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="14893-164">Voici les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="14893-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="14893-165">Quel site SharePoint voulez-vous utiliser pour le débogage de votre add-in ?</span><span class="sxs-lookup"><span data-stu-id="14893-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="14893-166">Spécifiez l’URL de votre site PWA, par https://contoso.sharepoint.com/sites/pwa exemple.</span><span class="sxs-lookup"><span data-stu-id="14893-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="14893-167">Comment souhaitez-vous héberger votre Add-in SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="14893-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="14893-168">Choose [X] **SharePoint-hosted**.</span><span class="sxs-lookup"><span data-stu-id="14893-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="14893-169">Pour plus d’informations sur les add-ins SharePoint, y compris sur les options d’hébergement, voir [Les add-ins SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="14893-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="14893-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="14893-170">Click **Next**.</span></span> 
    
<span data-ttu-id="14893-171">La deuxième boîte de dialogue supplémentaire vous demande de spécifier la version SharePoint Online pour le complément :</span><span class="sxs-lookup"><span data-stu-id="14893-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="14893-172">Quelle est la version la plus ancienne de SharePoint que vous souhaitez que votre add-in cible ?</span><span class="sxs-lookup"><span data-stu-id="14893-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="14893-173">Choose [X] S **harePoint-Online**.</span><span class="sxs-lookup"><span data-stu-id="14893-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="14893-174">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="14893-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="14893-175">Visual Studio crée le projet et accède au site Project Online.</span><span class="sxs-lookup"><span data-stu-id="14893-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="14893-176">Activer le chargement de version secondaire sur le site Project Online</span><span class="sxs-lookup"><span data-stu-id="14893-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="14893-177">Le chargement de version test est le mécanisme permettant de tester et de déboguer des add-ins Project Online. Vous avez besoin de deux scripts pour le chargement de version test : un pour activer le chargement de version test sur votre site Project Online et un autre pour désactiver le chargement de version test une fois que vous avez terminé le test et déboguer le module.</span><span class="sxs-lookup"><span data-stu-id="14893-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="14893-178">Pour plus d’informations sur la configuration du chargement indépendant, voir Activer le chargement indépendant d’application dans votre collection de [sites non-développeur.](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)</span><span class="sxs-lookup"><span data-stu-id="14893-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="14893-179">Le chargement indépendant d’applications est une fonctionnalité de développement/test.</span><span class="sxs-lookup"><span data-stu-id="14893-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="14893-180">Il **n’est pas destiné à une utilisation en production.**</span><span class="sxs-lookup"><span data-stu-id="14893-180">It is **not intended for production use**.</span></span> <span data-ttu-id="14893-181">Ne chargez pas les applications de manière régulière ou maintenez le chargement de version d’application activé plus longtemps que vous n’utilisez activement la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="14893-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="14893-182">Ajouter du contenu au projet de add-in</span><span class="sxs-lookup"><span data-stu-id="14893-182">Add content to the add-in project</span></span>

<span data-ttu-id="14893-183">Après la création d’un projet et la configuration du mécanisme de débogage, l’ajout de contenu à l’application comprend les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="14893-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="14893-184">Définition de l’étendue de l’application</span><span class="sxs-lookup"><span data-stu-id="14893-184">Setting the application scope</span></span>
    
- <span data-ttu-id="14893-185">Liaison de la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="14893-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="14893-186">Ajout d’éléments d’interface utilisateur au add-in</span><span class="sxs-lookup"><span data-stu-id="14893-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="14893-187">Initialisation et connexion au service Project Online</span><span class="sxs-lookup"><span data-stu-id="14893-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="14893-188">Récupération des projets et des détails/propriétés</span><span class="sxs-lookup"><span data-stu-id="14893-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="14893-189">Affichage des projets</span><span class="sxs-lookup"><span data-stu-id="14893-189">Displaying projects</span></span>
    
- <span data-ttu-id="14893-190">Affichage des tâches pour un projet</span><span class="sxs-lookup"><span data-stu-id="14893-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="14893-191">Le projet de add-in se compose de nombreux fichiers.</span><span class="sxs-lookup"><span data-stu-id="14893-191">The add-in project consists of many files.</span></span> <span data-ttu-id="14893-192">Dans cet exemple, vous devez modifier les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="14893-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="14893-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="14893-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="14893-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="14893-194">Default.aspx</span></span>
    
- <span data-ttu-id="14893-195">App.js</span><span class="sxs-lookup"><span data-stu-id="14893-195">App.js</span></span>
    
- <span data-ttu-id="14893-196">App.css - facultatif ; contient des définitions de style développées pour le add-in</span><span class="sxs-lookup"><span data-stu-id="14893-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="14893-197">Si le client Project Online change, par exemple en passant d’une version d’essai à un site d’abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion au serveur et l’URL du site, à l’aide de la fenêtre Propriétés disponible via la commande Fenêtre Afficher les   >   propriétés.</span><span class="sxs-lookup"><span data-stu-id="14893-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="14893-198">Vous pouvez également ajouter des fichiers au projet.</span><span class="sxs-lookup"><span data-stu-id="14893-198">You can also add files to the project.</span></span> <span data-ttu-id="14893-199">Si c’est le cas, vous devez mettre à jour le fichier Elements.xml situé dans le même groupe (contenu, images, pages ou scripts) pour inclure les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="14893-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="14893-200">Pour plus d’informations sur les fichiers de projet, voir Explorer la structure du manifeste de l’application et le package d’un [add-in SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)</span><span class="sxs-lookup"><span data-stu-id="14893-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="14893-201">Définir l’étendue de l’application</span><span class="sxs-lookup"><span data-stu-id="14893-201">Set application scope</span></span>

<span data-ttu-id="14893-202">Le add-in a besoin de niveaux d’étendue ou d’autorisation définis avant que le service renvoie des informations dans les résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="14893-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="14893-203">Pour ce module, utilisez l’étendue suivante pour Visual Studio projet.</span><span class="sxs-lookup"><span data-stu-id="14893-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="14893-204">Cette modification est réalisée dans le fichier AppManifest.xml sous l’onglet Autorisations :</span><span class="sxs-lookup"><span data-stu-id="14893-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="14893-205">Domaine d’application</span><span class="sxs-lookup"><span data-stu-id="14893-205">Scope</span></span>|<span data-ttu-id="14893-206">Autorisation</span><span class="sxs-lookup"><span data-stu-id="14893-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="14893-207">Projets multiples (Project Server)</span><span class="sxs-lookup"><span data-stu-id="14893-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="14893-208">Lire</span><span class="sxs-lookup"><span data-stu-id="14893-208">Read</span></span>  <br/> |
   
<span data-ttu-id="14893-209">Enregistrez le fichier après avoir définir l’étendue de l’application.</span><span class="sxs-lookup"><span data-stu-id="14893-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="14893-210">Sinon, aucune donnée n’est renvoyée à partir du service.</span><span class="sxs-lookup"><span data-stu-id="14893-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="14893-211">Lier la bibliothèque JSOM</span><span class="sxs-lookup"><span data-stu-id="14893-211">Link the JSOM library</span></span>

<span data-ttu-id="14893-212">Les bibliothèques Project Online runtime, PS.js et PS.debug.js, sont fournies par Project Online et sont toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="14893-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="14893-213">Les add-ins JavaScript qui utilisent JSOM doivent établir un lien avec l’une de ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="14893-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="14893-214">Les définitions de liaison sont ajoutées dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="14893-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="14893-215">Les commandes d’utilisation des PS.js et/ou PS.debug.js font partie du code situé dans App.js fichier.</span><span class="sxs-lookup"><span data-stu-id="14893-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="14893-216">Ajoutez la commande suivante pour PS.js définition PS.debug.js dans l’élément qui suit «  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` SharePoint:ScriptLink » pour sp.js.</span><span class="sxs-lookup"><span data-stu-id="14893-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="14893-217">**L’attribut OnDemand** pour PS.js ou PS.debug.js sur **false**.</span><span class="sxs-lookup"><span data-stu-id="14893-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="14893-218">Ajouter des éléments d’interface utilisateur au add-in</span><span class="sxs-lookup"><span data-stu-id="14893-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="14893-219">L’exemple de add-in se compose de quelques composants.</span><span class="sxs-lookup"><span data-stu-id="14893-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="14893-220">Les descriptions des éléments statiques se trouvent dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="14893-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="14893-221">Les descriptions des éléments dynamiques et le code de tous les composants se trouvent dans App.js fichier.</span><span class="sxs-lookup"><span data-stu-id="14893-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="14893-222">Pour obtenir des commentaires sur les composants, reportez-vous aux listes de code source.</span><span class="sxs-lookup"><span data-stu-id="14893-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="14893-223">Voici la liste des composants de l’interface utilisateur dans le composant :</span><span class="sxs-lookup"><span data-stu-id="14893-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="14893-224">Titre</span><span class="sxs-lookup"><span data-stu-id="14893-224">Title</span></span>
    
- <span data-ttu-id="14893-225">Introduction du verbiage</span><span class="sxs-lookup"><span data-stu-id="14893-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="14893-226">Bouton pour supprimer des tâches du tableau</span><span class="sxs-lookup"><span data-stu-id="14893-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="14893-227">Tableau répertoriant l’ID et le nom du projet, ainsi que les informations sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="14893-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="14893-228">Bouton Tâches (cloné une fois pour chaque projet) qui importe les données de tâche dans la table.</span><span class="sxs-lookup"><span data-stu-id="14893-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="14893-229">Pour plus d’informations sur l’interface utilisateur, telles que le titre et la partie en-tête de la table de projet, voir le fichier de projet Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="14893-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="14893-230">Initialiser et se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="14893-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="14893-231">Le App.js contient le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="14893-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="14893-232">Le add-in charge PS.js dans le navigateur, puis appelle la fonction initializePage.</span><span class="sxs-lookup"><span data-stu-id="14893-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="14893-233">InitializePage récupère un contexte au point de terminaison Project Online et démarre la fonction loadProjects.</span><span class="sxs-lookup"><span data-stu-id="14893-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="14893-234">Récupérer les projets</span><span class="sxs-lookup"><span data-stu-id="14893-234">Retrieve the projects</span></span>

<span data-ttu-id="14893-235">La fonction loadProjects interroge le service pour les noms de projet et les ID.</span><span class="sxs-lookup"><span data-stu-id="14893-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="14893-236">L’application récupère le nom du projet et l’ID de projet. D’autres informations sur le projet sont disponibles et sont accessibles en modifiant la méthode de chargement pour identifier explicitement les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="14893-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="14893-237">Un exemple est fourni dans le code en tant que commentaire.</span><span class="sxs-lookup"><span data-stu-id="14893-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="14893-238">Si la requête réussit, le add-in continue en appelant displayProjects.</span><span class="sxs-lookup"><span data-stu-id="14893-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="14893-239">Afficher les projets</span><span class="sxs-lookup"><span data-stu-id="14893-239">Display the projects</span></span>

<span data-ttu-id="14893-240">La fonction displayProjects crée un tableau, une ligne par projet et un bouton pour afficher les tâches pour le projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="14893-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="14893-241">La boucle While accède aux propriétés d’ID et de nom.</span><span class="sxs-lookup"><span data-stu-id="14893-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="14893-242">Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés.</span><span class="sxs-lookup"><span data-stu-id="14893-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="14893-243">Afficher les tâches d’un projet</span><span class="sxs-lookup"><span data-stu-id="14893-243">Display the tasks for a project</span></span>

<span data-ttu-id="14893-244">Les tâches, qui font partie du add-in, ne font pas partie du chargement initial.</span><span class="sxs-lookup"><span data-stu-id="14893-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="14893-245">Si l’utilisateur est intéressé par les tâches associées à un projet, le fait de cliquer sur le bouton « Afficher les tâches » entraîne l’affichage des tâches dans la liste à l’aide du handler d’événement btnLoadTasks.</span><span class="sxs-lookup"><span data-stu-id="14893-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="14893-246">Le handler d’événement btnLoadTasks, avec l’ID de projet approprié, demande les tâches pour le projet spécifié au serveur.</span><span class="sxs-lookup"><span data-stu-id="14893-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="14893-247">Une fois récupéré, btnLoadTasks transmet la liste des tâches à displayTasks pour présenter les tâches à l’écran.</span><span class="sxs-lookup"><span data-stu-id="14893-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="14893-248">La fonction displayTasks affiche les tâches associées à un projet spécifié immédiatement sous l’entrée du projet.</span><span class="sxs-lookup"><span data-stu-id="14893-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="14893-249">La boucle While accède à l’ID de tâche et aux propriétés de nom.</span><span class="sxs-lookup"><span data-stu-id="14893-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="14893-250">Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés.</span><span class="sxs-lookup"><span data-stu-id="14893-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="14893-251">Un exemple de sortie pour les tâches d’un seul projet suit.</span><span class="sxs-lookup"><span data-stu-id="14893-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="14893-252">![Capture d’écran montrant la sortie d’une tâche]de projet Capture d’écran(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "montrant la sortie d’une tâche de projet")</span><span class="sxs-lookup"><span data-stu-id="14893-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14893-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14893-253">See also</span></span>

<span data-ttu-id="14893-254">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="14893-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


