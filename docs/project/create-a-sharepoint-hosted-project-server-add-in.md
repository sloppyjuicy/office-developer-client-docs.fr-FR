---
title: Créer un complément Project Server hébergé sur SharePoint
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Parmi les trois types d’applications que vous pouvez créer pour Project Online (auto-hébergé, hébergé par un fournisseur et hébergé par SharePoint), l’application hébergée par SharePoint est la plus simple à créer et à déployer.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773756"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a><span data-ttu-id="8c2b6-103">Créer un complément Project Server hébergé sur SharePoint</span><span class="sxs-lookup"><span data-stu-id="8c2b6-103">Create a SharePoint-hosted Project Server add-in</span></span>

<span data-ttu-id="8c2b6-104">Parmi les trois types d’applications que vous pouvez créer pour Project Online (auto-hébergé, hébergé par un fournisseur et hébergé par SharePoint), l’application hébergée par SharePoint est la plus simple à créer et à déployer.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-104">Of the three types of apps that you can create for Project Online (autohosted, provider-hosted, and SharePoint-hosted), the SharePoint-hosted app is the simplest to create and deploy.</span></span> <span data-ttu-id="8c2b6-105">Une application hébergée sur SharePoint ne requiert pas d’authentification OAuth et n’utilise pas Azure ou nécessite la maintenance d’un site local pour les ressources hébergées par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-105">A SharePoint-hosted app does not require OAuth authentication, and does not use Azure or require maintenance of a local site for the provider-hosted resources.</span></span> <span data-ttu-id="8c2b6-106">Le modèle **App pour SharePoint 2013** dans Visual Studio est une infrastructure pratique pour le développement d’applications qui peuvent être publiées et vendues dans l’Office Store ou déployées sur un catalogue d’applications privé sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-106">The **App for SharePoint 2013** template in Visual Studio is a convenient framework for developing apps that can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> 
  
<span data-ttu-id="8c2b6-107">Dans Project, l’État est un processus dans lequel un membre de l’équipe peut utiliser la page tâches dans Project Web App pour envoyer l’état d’une tâche affectée, comme le nombre d’heures travaillées chaque jour de la semaine consacré à la tâche.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-107">In Project, statusing is a process where a team member can use the Tasks page in Project Web App to submit the status of an assigned task, such as the number of hours worked each day of a week spent working on the task.</span></span> <span data-ttu-id="8c2b6-108">Le propriétaire de l’affectation (généralement, le responsable de projet) peut approuver ou rejeter l’état.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-108">The assignment owner (usually the project manager) can approve or reject the status.</span></span> <span data-ttu-id="8c2b6-109">Lorsque celui-ci est approuvé, Project recalcule la planification.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-109">When the status is approved, Project recalculates the schedule.</span></span> <span data-ttu-id="8c2b6-110">L’application **QuickStatus** affiche les tâches affectées, où l’utilisateur peut rapidement mettre à jour le pourcentage achevé et envoyer l’état des affectations sélectionnées pour approbation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-110">The **QuickStatus** app displays assigned tasks, where the user can quickly update percent complete and submit status of the selected assignments for approval.</span></span> <span data-ttu-id="8c2b6-111">Bien que la page tâches de Project Web App offre bien plus de fonctionnalités, l’application **QuickStatus** est un exemple qui fournit une interface simplifiée.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-111">Although the Tasks page in Project Web App has much more functionality, the **QuickStatus** app is an example that provides a simplified interface.</span></span> 
  
<span data-ttu-id="8c2b6-112">L’application **QuickStatus** est un exemple pour les développeurs ; Il n’est pas destiné à être utilisé dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-112">The **QuickStatus** app is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="8c2b6-113">L’objectif principal est de présenter un exemple de développement d’applications pour Project Online, mais pas de créer une application d’État entièrement fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-113">The primary purpose is to show an example of app development for Project Online, not to create a fully functional statusing app.</span></span> <span data-ttu-id="8c2b6-114">Pour une meilleure approche de l’État, consultez la recommandation dans les [étapes suivantes](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-114">For a better approach to statusing, see the recommendation in [Next steps](#pj15_StatusingApp_NextSteps).</span></span>
  
<span data-ttu-id="8c2b6-115">Pour obtenir des informations générales sur l’État, consultez l' [avancement des tâches](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-115">For general information about statusing, see [Task progress](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span></span> <span data-ttu-id="8c2b6-116">Pour plus d’informations sur le développement de compléments pour SharePoint et Project Server, reportez-vous à la rubrique [compléments SharePoint](https://msdn.microsoft.com/library/jj163230.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-116">For more information about developing add-ins for SharePoint and Project Server, see [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).</span></span>

<span data-ttu-id="8c2b6-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span></span>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a><span data-ttu-id="8c2b6-118">Conditions préalables à la création d’une application pour Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c2b6-118">Prerequisites for creating an app for Project Server 2013</span></span>

<span data-ttu-id="8c2b6-119">Pour développer des applications relativement simples qui peuvent être déployées sur Project Online ou sur une installation locale de Project Server 2013, vous pouvez utiliser le Napa, qui fournit un environnement de développement en ligne.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-119">To develop relatively simple apps that can be deployed to Project Online or to an on-premises installation of Project Server 2013, you can use the Napa, which provide an online development environment.</span></span> <span data-ttu-id="8c2b6-120">Pour les applications plus complexes, la modification du ruban Project Web App et le débogage plus facile lors du développement, vous pouvez utiliser Visual Studio 2012 ou Visual Studio 2013.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-120">For more complex apps, modifying the Project Web App ribbon, and easier debugging during development, you can use Visual Studio 2012 or Visual Studio 2013.</span></span> <span data-ttu-id="8c2b6-121">Par exemple, avec une installation locale, vous pouvez vérifier manuellement les modifications des DataTables brouillons dans la base de données Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-121">For example, with an on-premises installation, you can manually check the Drafts datatables for changes in the Project Server database.</span></span> <span data-ttu-id="8c2b6-122">Cet article explique comment développer des applications avec Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-122">This article shows how to do app development with Visual Studio.</span></span>
  
<span data-ttu-id="8c2b6-123">Le développement d’applications Project Server avec Visual Studio nécessite les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-123">Development of Project Server apps with Visual Studio requires the following:</span></span>
  
- <span data-ttu-id="8c2b6-p106">Assurez-vous d’avoir installé les mises à jour Windows et les Service Packs les plus récents sur votre ordinateur de développement local. Le système d’exploitation peut être Windows 7, Windows 8, Windows Server 2008 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p106">Ensure that you have installed the most recent service packs and Windows updates on your local development computer. The operating system can be Windows 7, Windows 8, Windows Server 2008, or Windows Server 2012.</span></span>
    
- <span data-ttu-id="8c2b6-126">Vous devez disposer d’un ordinateur sur lequel SharePoint Server 2013 et Project Server 2013 sont installés, où l’ordinateur est configuré pour l’isolation des applications et la chargement des applications.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-126">You must have a computer that has SharePoint Server 2013 and Project Server 2013 installed, where the computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="8c2b6-127">Le chargement de version test permet à Visual Studio d’installer temporairement l’application pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-127">Sideloading enables Visual Studio to temporarily install the app for debugging.</span></span> <span data-ttu-id="8c2b6-128">Vous pouvez utiliser une installation locale de SharePoint et Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-128">You can use an on-premises installation of SharePoint and Project Server.</span></span> <span data-ttu-id="8c2b6-129">Pour plus d’informations, reportez-vous à [configurer un environnement de développement local pour les applications pour SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-129">For more information, see [Set up an on-premises development environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-130">Pour une installation locale, configurez un domaine d’application isolé *avant* de créer un catalogue d’applications d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-130">For an on-premises installation, configure an isolated app domain  *before*  you create a corporate app catalog.</span></span> 
  
- <span data-ttu-id="8c2b6-131">L’ordinateur de développement peut être un ordinateur distant sur lequel sont installés les outils de développement Office pour Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-131">The development computer can be a remote computer that has Office Developer Tools for Visual Studio 2012 installed.</span></span> <span data-ttu-id="8c2b6-132">Assurez-vous que vous avez installé la version la plus récente ; reportez-vous à la section *Outils* des [téléchargements d’applications pour Office et SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-132">Ensure that you have installed the most recent version; see the  *Tools*  section of the [Apps for Office and SharePoint downloads](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span></span>
    
- <span data-ttu-id="8c2b6-133">Vérifiez que l’instance de Project Web App que vous allez utiliser pour le développement et le test est accessible dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-133">Verify that the Project Web App instance you will be using for development and testing is accessible in the browser.</span></span>
    
<span data-ttu-id="8c2b6-134">Pour plus d’informations sur l’utilisation des outils en ligne, voir [configurer un environnement pour le développement d’applications pour SharePoint sur Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-134">For information about using the online tools, see [Set up an environment for developing apps for SharePoint on Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span></span> <span data-ttu-id="8c2b6-135">Pour obtenir une procédure pas à pas de création d’une application simple pour Project Server qui utilise les outils en ligne, consultez la série de blogs EPMSource, [Building Your First Project Server App](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-135">For a walkthrough of building a simple app for Project Server that uses the online tools, see the EPMSource blog series, [Building your first Project Server app](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span></span>

<span data-ttu-id="8c2b6-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span></span>

## <a name="using-visual-studio-to-create-a-project-server-app"></a><span data-ttu-id="8c2b6-137">Utilisation de Visual Studio pour créer une application Project Server</span><span class="sxs-lookup"><span data-stu-id="8c2b6-137">Using Visual Studio to create a Project Server app</span></span>

<span data-ttu-id="8c2b6-138">Les outils de développement Office pour Visual Studio 2012 incluent un modèle pour les applications SharePoint qui peuvent être utilisées avec Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-138">Office Developer Tools for Visual Studio 2012 includes a template for SharePoint apps that can be used with Project Server 2013.</span></span> <span data-ttu-id="8c2b6-139">Lorsque vous créez une solution d’application, celle-ci inclut les fichiers suivants pour votre code personnalisé :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-139">When you create an app solution, the solution includes the following files for your custom code:</span></span>
  
- <span data-ttu-id="8c2b6-p111">**AppManifest.xml** comprend des paramètres pour le titre de l’application, l’étendue de demande d’autorisation et d’autres propriétés. La procédure 1 inclut les étapes pour définir les propriétés à l’aide du concepteur de manifeste.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p111">**AppManifest.xml** includes settings for the app title, permission request scope, and other properties. Procedure 1 includes steps to set the properties by using the Manifest Designer.</span></span> 
    
- <span data-ttu-id="8c2b6-142">**Default.aspx** dans le dossier Pages est la page principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-142">**Default.aspx** in the Pages folder is the main page of the app.</span></span> <span data-ttu-id="8c2b6-143">La procédure 2 décrit comment ajouter du contenu HTML5 à l’application **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-143">Procedure 2 shows how to add HTML5 content for the **QuickStatus** app.</span></span> 
    
- <span data-ttu-id="8c2b6-144">**App. js** dans le dossier scripts est le fichier principal du code JavaScript personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-144">**App.js** in the Scripts folder is the primary file for the custom JavaScript code.</span></span> <span data-ttu-id="8c2b6-145">La procédure 3 décrit le code JavaScript pour l’application **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-145">Procedure 3 explains the JavaScript code for the **QuickStatus** app.</span></span> 
    
   <span data-ttu-id="8c2b6-146">Si vous ajoutez des contrôles commerciaux tels qu’une grille jQuery ou un sélecteur de date, vous pouvez ajouter des références à des fichiers JavaScript supplémentaires dans le fichier default. aspx.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-146">If you add commercial controls such as a jQuery-based grid or date picker, you can add references to additional JavaScript files in the Default.aspx file.</span></span>
    
- <span data-ttu-id="8c2b6-147">\*\*App.css \*\* dans le dossier Contenu est le principal fichier pour les styles personnalisés CSS3.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-147">**App.css** in the Content folder is the primary file for custom CSS3 styles.</span></span> <span data-ttu-id="8c2b6-148">Les procédures 2 et 3 comprennent des informations sur les feuilles de style en cascade (CSS) pour l’application **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-148">Procedure 2 and Procedure 3 include information about cascading style sheets (CSS) styles for the **QuickStatus** app.</span></span> <span data-ttu-id="8c2b6-149">Vous pouvez ajouter des références supplémentaires aux fichiers CSS dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-149">You can add references to additional CSS files in the Default.aspx file.</span></span> 
    
- <span data-ttu-id="8c2b6-150">**AppIcon. png** dans le dossier images est l’icône 96 x 96 que l’application affiche dans l’Office Store ou le catalogue d’applications.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-150">**AppIcon.png** in the Images folder is the 96 x 96 icon that the app displays in the Office Store or the app catalog.</span></span> 
    
<span data-ttu-id="8c2b6-151">Pour modifier le ruban Project Web App, vous pouvez ajouter une action personnalisée de ruban.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-151">To modify the Project Web App ribbon, you can add a ribbon custom action.</span></span> <span data-ttu-id="8c2b6-152">La section [Exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example) contient le code complet pour les fichiers Default.aspx, App.js, App.css, Elements.xml et AppManifest.xml modifiés.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-152">The [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section includes the complete code for the modified Default.aspx, App.js, App.css, Elements.xml, and AppManifest.xml files.</span></span> 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a><span data-ttu-id="8c2b6-153">Procédure 1.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-153">Procedure 1.</span></span> <span data-ttu-id="8c2b6-154">Pour créer un projet d’application dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8c2b6-154">To create an app project in Visual Studio</span></span>

1. <span data-ttu-id="8c2b6-155">Exécutez Visual Studio 2012 en tant qu’administrateur, puis sélectionnez **nouveau projet** sur la page de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-155">Run Visual Studio 2012 as an administrator, and then select **New Project** on the Start page.</span></span> 
    
2. <span data-ttu-id="8c2b6-p117">Dans la boîte de dialogue **Nouveau projet**, développez les nœuds **Modèles**, **Visual C#** et **Office/SharePoint**, puis sélectionnez **Applications**. Utilisez l’option **.NET Framework 4.5** par défaut dans la liste déroulante de l’infrastructure cible en haut du volet central, puis sélectionnez **Application pour Office 2013** (voir la figure 1).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p117">In the **New Project** dialog box, expand the **Templates**, **Visual C#**, and **Office/SharePoint** nodes, and then select **Apps**. Use the default **.NET Framework 4.5** in the target framework drop-down list at the top of the center pane, and then select **App for SharePoint 2013** (see Figure 1).</span></span> 
    
3. <span data-ttu-id="8c2b6-158">Dans le champ **nom** , tapez QuickStatus, accédez à l’emplacement où vous souhaitez enregistrer l’application, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-158">In the **Name** field, type QuickStatus, browse to the location where you want to save the app, and then choose **OK**.</span></span>
    
   <span data-ttu-id="8c2b6-159">**Figure 1. Création d’une application Project Server dans Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-159">**Figure 1. Creating a Project Server app in Visual Studio**</span></span>

   <span data-ttu-id="8c2b6-160">![Création d’une application Project Server dans Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Création d’une application Project Server dans Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-160">![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")</span></span>
  
4. <span data-ttu-id="8c2b6-161">Dans la boîte de dialogue **Nouvelle application pour SharePoint**, renseignez les trois champs suivants :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-161">In the **New app for SharePoint** dialog box, fill in the following three fields:</span></span> 
    
   - <span data-ttu-id="8c2b6-162">Dans la zone de texte supérieure, tapez le nom que vous souhaitez que l’application affiche dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-162">In the top text box, type the name that you want the app to display in Project Web App.</span></span> <span data-ttu-id="8c2b6-163">Par exemple, saisissez Mise à jour de QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-163">For example, type Quick Status Update.</span></span>
    
   - <span data-ttu-id="8c2b6-164">Pour le site à utiliser pour le débogage, tapez l’URL de l’instance Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-164">For the site to use for debugging, type the URL of the Project Web App instance.</span></span> <span data-ttu-id="8c2b6-165">Par exemple, tapez `https://ServerName/ProjectServerName` (remplacez _ServerName_ et _ProjectServerName_ par vos propres valeurs), puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-165">For example, type  `https://ServerName/ProjectServerName` (replacing  _ServerName_ and  _ProjectServerName_ with your own values), and then choose **Validate**.</span></span> <span data-ttu-id="8c2b6-166">Si tout se passe bien, Visual Studio affiche **Connexion réussie**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-166">If all goes well, Visual Studio shows **Connection successful**.</span></span> <span data-ttu-id="8c2b6-167">Si vous obtenez un message d’erreur, vérifiez que l’URL de Project Web App est correcte et que l’ordinateur Project Server est configuré pour l’isolation de l’application et chargement des applications.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-167">If you get an error message, ensure that the Project Web App URL is correct and that the Project Server computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="8c2b6-168">Pour plus d’informations, reportez-vous à la section [conditions préalables à la création d’une application pour Project Server 2013](#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-168">For more information, see the [Prerequisites for creating an app for Project Server 2013](#pj15_StatusingApp_Prerequisites) section.</span></span> 
    
   - <span data-ttu-id="8c2b6-169">Dans la liste déroulante **Comment souhaitez-vous héberger votre application pour SharePoint ?**, choisissez **Hébergement par SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-169">In the **How do you want to host your app for SharePoint** drop-down list, choose **SharePoint-hosted**.</span></span>
    
   > [!CAUTION]
   > <span data-ttu-id="8c2b6-170">Si vous choisissez le type de projet par défaut **Hébergement par le fournisseur** par erreur, Visual Studio crée deux projets dans la solution : un projet **QuickStatus** et un projet **QuickStatusWeb**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-170">If you choose the default **Provider-hosted** project type by mistake, Visual Studio creates two projects in the solution: a **QuickStatus** project and a **QuickStatusWeb** project.</span></span> <span data-ttu-id="8c2b6-171">Si deux projets apparaissent, supprimez cette solution et recommencez.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-171">If you see two projects, delete that solution and start again.</span></span> 
  
5. <span data-ttu-id="8c2b6-172">Choisissez **OK** pour créer la solution **QuickStatus**, le projet **QuickStatus** et les fichiers par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-172">Choose **OK** to create the **QuickStatus** solution, **QuickStatus** project, and default files.</span></span> 
    
6. <span data-ttu-id="8c2b6-p121">Ouvrez le concepteur de manifeste (par exemple, double-cliquez sur le fichier AppManifest.xml). Sur l’onglet **Général**, la zone de texte **Titre** doit afficher le nom de l’application saisi à l’étape 4. Choisissez l’onglet **Autorisations** afin d’ajouter les demandes d’autorisation suivantes pour l’application (voir figure 2) :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p121">Open the Manifest Designer view (for example, double-click the AppManifest.xml file). On the **General** tab, the **Title** text box should show the app name that you typed in step 4. Choose the **Permissions** tab to add the following permission requests for the app (see Figure 2):</span></span> 
    
   - <span data-ttu-id="8c2b6-p122">Sur la première ligne de la liste **Demandes d’autorisation** dans la colonne **Étendue**, choisissez **État** dans la liste déroulante. Dans la colonne **Autorisation**, choisissez **SubmitStatus**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p122">In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list. In the **Permission** column, choose **SubmitStatus**.</span></span>
    
   - <span data-ttu-id="8c2b6-178">Ajoutez une ligne là où l’option **Étendue** est définie sur **Plusieurs projets** et où **Autorisation** est définie sur **Lecture**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-178">Add a row where the **Scope** is **Multiple Projects** and the **Permission** is **Read**.</span></span>
    
   <span data-ttu-id="8c2b6-179">**Figure 2. Définition de l’étendue des autorisations pour une application d’état**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-179">**Figure 2. Setting the permission scope for a statusing app**</span></span>

   <span data-ttu-id="8c2b6-180">![Définition de l’étendue des autorisations pour une application d’état](media/pj15_CreateStatusingApp_PermissionScope.gif "Définition de l’étendue des autorisations pour une application d’état")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-180">![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")</span></span>
  
<span data-ttu-id="8c2b6-181">L’application **QuickStatus** permet à un utilisateur Project Web App de lire les devoirs de cet utilisateur à partir de plusieurs projets, de modifier le pourcentage d’achèvement de l’affectation et de soumettre la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-181">The **QuickStatus** app enables a Project Web App user to read assignments for that user from multiple projects, change the assignment percent complete, and submit the update.</span></span> <span data-ttu-id="8c2b6-182">Les autres étendues de demande d’autorisation figurant dans la liste déroulante de la figure 2 ne sont pas requises pour cette application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-182">The other permission request scopes shown in the drop-down list in Figure 2 are not required for this app.</span></span> <span data-ttu-id="8c2b6-183">Les étendues de demande d’autorisation sont les autorisations demandées par l’application pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-183">The permission request scopes are the permissions that the app requests on behalf of the user.</span></span> <span data-ttu-id="8c2b6-184">Si l’utilisateur ne dispose pas de ces autorisations dans Project Web App, l’application ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-184">If the user does not have those permissions in Project Web App, the app does not run.</span></span> <span data-ttu-id="8c2b6-185">Une application peut avoir plusieurs étendues de demande d’autorisation, y compris celles des autres autorisations SharePoint, mais doit avoir uniquement le minimum requis pour la fonctionnalité de l’application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-185">An app can have multiple permission request scopes, including those for other SharePoint permissions, but should have only the minimum necessary for the app functionality.</span></span> <span data-ttu-id="8c2b6-186">Voici les étendues de demande d’autorisation qui sont liées à Project Server :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-186">Following are the permission request scopes that are related to Project Server:</span></span> 

- <span data-ttu-id="8c2b6-187">**Ressources d’entreprise**: autorisations du gestionnaire de ressources, pour lire ou écrire des informations sur d’autres utilisateurs Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-187">**Enterprise Resources**: Resource manager permissions, to read or write information about other Project Web App users.</span></span>
    
- <span data-ttu-id="8c2b6-188">**Plusieurs projets** : lecture ou écriture pour plusieurs projets, pour lesquels l’utilisateur dispose des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-188">**Multiple Projects**: Read or write to more than one project, where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="8c2b6-189">**Project Server**: requiert que l’utilisateur de l’application dispose des autorisations d’administrateur pour Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-189">**Project Server**: Requires the app user to have administrator permissions for Project Web App.</span></span>
    
- <span data-ttu-id="8c2b6-190">**Création de rapports**: Lisez le service OData **ProjectData** pour Project Web App (nécessite uniquement une autorisation d’ouverture de session pour Project Web App).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span></span> 
    
- <span data-ttu-id="8c2b6-191">**Projet unique** : lecture ou écriture pour un projet pour lequel l’utilisateur dispose des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-191">**Single Project**: Read or write to a project where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="8c2b6-192">**État** : envoi de mises à jour d’état des affectations, telles que les heures travaillées, le pourcentage achevé et les nouvelles affectations.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-192">**Statusing**: Submit updates for status of assignments, such as times worked, percent complete, and new assignments.</span></span>
    
- <span data-ttu-id="8c2b6-193">**Flux de travail** : si l’utilisateur est autorisé à exécuter des flux de travail Project Server, l’application s’exécute ensuite avec des autorisations élevées pour le flux de travail.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-193">**Workflow**: If the user has permission to run Project Server workflows, the app then runs with elevated permissions for the workflow.</span></span>
    
<span data-ttu-id="8c2b6-194">Pour plus d’informations sur les étendues de demande d’autorisation pour Project Server 2013, voir la section *applications de projet* dans [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md) and [app permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-194">For more information about permission request scopes for Project Server 2013, see the  *Project apps*  section in [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) and [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span></span>


<span data-ttu-id="8c2b6-195"><a name="pj15_StatusingApp_HTML"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-195"><a name="pj15_StatusingApp_HTML"> </a></span></span>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a><span data-ttu-id="8c2b6-196">Création de contenu HTML pour l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-196">Creating the HTML content for the QuickStatus app</span></span>

<span data-ttu-id="8c2b6-197">Avant de commencer à coder le contenu HTML, concevez l’interface utilisateur et l’expérience utilisateur pour l’application QuickStatus (la figure 3 montre un exemple de la page terminée).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-197">Before you start coding the HTML content, design the user interface and user experience for the QuickStatus app (Figure 3 shows an example of the completed page).</span></span> <span data-ttu-id="8c2b6-198">Une conception peut également inclure un plan des fonctions JavaScript qui interagissent avec le code HTML.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-198">A design can also include an outline of the JavaScript functions that interact with the HTML code.</span></span> <span data-ttu-id="8c2b6-199">Pour plus d’informations, voir [conception de l’expérience utilisateur pour les applications dans SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-199">For general information, see [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span></span>
  
<span data-ttu-id="8c2b6-200">**Figure 3. Conception de la page d’application QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-200">**Figure 3. Design of the QuickStatus app page**</span></span>

<span data-ttu-id="8c2b6-201">![Conception de la page d’application QuickStatus](media/pj15_CreateStatusingApp_AfterRefresh.gif "Conception de la page d’application QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-201">![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")</span></span>
  
<span data-ttu-id="8c2b6-202">L’application affiche le nom complet en haut, qui est la valeur de l’élément **Title** dans AppManifest.Xml.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-202">The app shows the display name at the top, which is the value of the **Title** element in AppManifest.xml.</span></span> 
  
<span data-ttu-id="8c2b6-203">Par défaut, la page utilise HTML5.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-203">By default, the page uses HTML5.</span></span> <span data-ttu-id="8c2b6-204">Voici les éléments HTML standard pour les objets de l’interface utilisateur principale contenus par l’application **QuickStatus** dans le corps de la page :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-204">Following are the standard HTML elements for the main UI objects that the **QuickStatus** app contains in the body of the page:</span></span> 
  
- <span data-ttu-id="8c2b6-205">Un élément **form** contient tous les autres éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-205">A **form** element contains all of the other UI elements.</span></span> 
    
- <span data-ttu-id="8c2b6-206">Un élément **fieldset** crée un conteneur et la bordure du tableau des affectations. L’élément enfant **legend** fournit une étiquette pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-206">A **fieldset** element creates a container and border for the table of assignments; the child **legend** element provides a label for the container.</span></span> 
    
- <span data-ttu-id="8c2b6-207">Un élément **table** inclut une légende et seulement un en-tête de tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-207">A **table** element includes a caption and only a table header.</span></span> <span data-ttu-id="8c2b6-208">Les fonctions JavaScript modifient la légende de tableau et ajoutent des lignes pour les affectations.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-208">JavaScript functions change the table caption and add rows for the assignments.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-209">Pour ajouter facilement une pagination et un tri, une application de production utilisera probablement un contrôle commercial de grille basée sur jQuery plutôt qu’un tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-209">To easily add paging and sorting, a production app would probably use a commercial jQuery-based grid control instead of a table.</span></span> 
  
   <span data-ttu-id="8c2b6-210">Le tableau contient les colonnes pour le nom du projet, le nom de la tâche avec une case à cocher, le travail réel, le pourcentage achevé, le travail restant et la date de fin de l’affectation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-210">The table includes columns for the project name, task name with a check box, actual work, percent complete, remaining work, and the assignment finish date.</span></span> <span data-ttu-id="8c2b6-211">Fonctions JavaScript créez la case à cocher et le champ d’entrée de texte pour le pourcentage d’achèvement de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-211">JavaScript functions create the check box and the text input field for the percent complete of each task.</span></span>
    
- <span data-ttu-id="8c2b6-212">Un élément **input** pour une zone de texte définit le pourcentage achevé pour toutes les affectations sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-212">An **input** element for a text box sets percent complete for all selected assignments.</span></span> 
    
- <span data-ttu-id="8c2b6-213">Un élément **button** envoie les modifications d’état.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-213">A **button** element submits the status changes.</span></span> 
    
- <span data-ttu-id="8c2b6-214">Un élément **button** actualise la page.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-214">A **button** element refreshes the page.</span></span> 
    
- <span data-ttu-id="8c2b6-215">Un élément **Button** quitte l’application et revient à la page tâches dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-215">A **button** element exits the app and returns to the Tasks page in Project Web App.</span></span> 
    
<span data-ttu-id="8c2b6-216">Les éléments de bouton et de zone de texte inférieurs se trouvent dans les éléments **div**, afin que les CSS puissent gérer facilement la position et l’apparence des objets d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-216">The bottom text box and button elements are within **div** elements, so that CSS can easily manage the position and appearance of the UI objects.</span></span> <span data-ttu-id="8c2b6-217">Une fonction JavaScript ajoute un paragraphe au bas de la page qui contient les résultats pour la réussite ou l’échec de la mise à jour de l’État.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-217">A JavaScript function adds a paragraph at the bottom of the page that contains results for success or failure of the status update.</span></span> 
  
### <a name="procedure-2-to-create-the-html-content"></a><span data-ttu-id="8c2b6-218">Procédure 2.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-218">Procedure 2.</span></span> <span data-ttu-id="8c2b6-219">Pour créer du contenu HTML</span><span class="sxs-lookup"><span data-stu-id="8c2b6-219">To create the HTML content</span></span>

1. <span data-ttu-id="8c2b6-220">Dans Visual Studio, ouvrez le fichier default. aspx.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-220">In Visual Studio, open the Default.aspx file.</span></span>
    
   <span data-ttu-id="8c2b6-221">Le fichier comprend deux éléments **asp : content** : l’élément avec l' `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribut est ajouté dans l’en-tête de page et l’élément `ContentPlaceHolderID="PlaceHolderMain"` avec l’attribut est placé dans l’élément **Body** de la page.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-221">The file includes two **asp:Content** elements: The element with the  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribute is added within the page header, and the element with the  `ContentPlaceHolderID="PlaceHolderMain"` attribute is placed within the page **body** element.</span></span> 
    
2. <span data-ttu-id="8c2b6-222">Dans le `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` contrôle de l’en-tête de page, ajoutez une référence au fichier PS. js sur l’ordinateur Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-222">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control for the page header, add a reference to the PS.js file on the Project Server computer.</span></span> <span data-ttu-id="8c2b6-223">Pour le test et le débogage, vous pouvez utiliser PS.debug.js.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-223">For testing and debugging, you can use PS.debug.js.</span></span> 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   <span data-ttu-id="8c2b6-224">L’infrastructure de l’application `/_layouts/15/` utilise le répertoire virtuel du site SharePoint dans les services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-224">The app infrastructure uses the `/_layouts/15/` virtual directory for the SharePoint site in IIS.</span></span> <span data-ttu-id="8c2b6-225">Le fichier physique est `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-225">The physical file is  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-226">Avant de déployer l’application pour une utilisation en production `.debug` , supprimez les références de script pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-226">Before you deploy the app for production use, remove  `.debug` from the script references to improve performance.</span></span> 
  
3. <span data-ttu-id="8c2b6-227">Dans le `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` contrôle du corps de la page, supprimez l’élément **div** généré, puis ajoutez le code HTML pour les objets de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-227">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control for the page body, delete the generated **div** element, and then add the HTML code for the UI objects.</span></span> <span data-ttu-id="8c2b6-228">L’élément **table** contient une ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-228">The **table** element contains only a header row.</span></span> <span data-ttu-id="8c2b6-229">La colonne **Nom de la tâche** inclut un contrôle d’entrée de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-229">The **Task name** column includes a check box input control.</span></span> <span data-ttu-id="8c2b6-230">Le texte pour l’élément **caption** est remplacé par le rappel **onGetUserNameSuccess** pour la fonction **getUserInfo** dans le fichier App.js.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-230">Text for the **caption** element is replaced by the **onGetUserNameSuccess** callback for the **getUserInfo** function in the App.js file.</span></span> 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. <span data-ttu-id="8c2b6-231">Dans le fichier App.css, ajoutez le code CSS pour la position et l’apparence des éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-231">In the App.css file, add CSS code for the position and appearance of the UI elements.</span></span> <span data-ttu-id="8c2b6-232">Pour obtenir le code CSS complet de l’application **QuickStatus**, consultez la section [Exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-232">For the complete CSS code of the **QuickStatus** app, see the [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section.</span></span> 
    
<span data-ttu-id="8c2b6-233">La procédure 3 ajoute les fonctions JavaScript pour lire les affectations et créer les lignes de tableau, et pour modifier et mettre à jour le pourcentage d’achèvement de l’affectation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-233">Procedure 3 adds the JavaScript functions to read the assignments and create the table rows, and to change and update the assignment percent complete.</span></span> <span data-ttu-id="8c2b6-234">Les étapes réelles sont plus itératives lors du développement d’une application, où vous pouvez également créer une partie du code HTML, ajouter et tester des styles et des fonctions JavaScript connexes, modifier ou ajouter du code HTML, puis répéter le processus.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-234">The actual steps are more iterative in developing an app, where you alternately create some of the HTML code, add and test related styles and JavaScript functions, modify or add more HTML code, and then repeat the process.</span></span>

<span data-ttu-id="8c2b6-235"><a name="pj15_StatusingApp_JavaScript"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-235"><a name="pj15_StatusingApp_JavaScript"> </a></span></span>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a><span data-ttu-id="8c2b6-236">Création des fonctions JavaScript pour l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-236">Creating the JavaScript functions for the QuickStatus app</span></span>

<span data-ttu-id="8c2b6-237">Le modèle Visual Studio pour une application SharePoint inclut le fichier App.js contenant le code d’initialisation par défaut qui obtient le contexte client SharePoint et illustre les actions de base d’obtention et de définition de la page d’application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-237">The Visual Studio template for a SharePoint app includes the App.js file, which contains default initialization code that gets the SharePoint client context and demonstrates basic get and set actions for the app page.</span></span> <span data-ttu-id="8c2b6-238">L’espace de noms JavaScript pour la bibliothèque SP. js côté client SharePoint est **SP**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-238">The JavaScript namespace for the SharePoint client-side SP.js library is **SP**.</span></span> <span data-ttu-id="8c2b6-239">Étant donné qu’une application Project Server utilise la bibliothèque PS.js, l’application utilise l’espace de noms **PS** pour obtenir le contexte client et accéder au JSOM pour Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-239">Because a Project Server app uses the PS.js library, the app uses the **PS** namespace to get the client context and access the JSOM for Project Server.</span></span> 
  
<span data-ttu-id="8c2b6-240">Les fonctions JavaScript dans l’application **QuickStatus** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-240">JavaScript functions in the **QuickStatus** app include the following:</span></span> 
  
- <span data-ttu-id="8c2b6-241">Le gestionnaire d’événements **ready** du document s’exécute lorsque le modèle objet de document (DOM) est instancié.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-241">The document **ready** event handler runs when the document object model (DOM) is instantiated.</span></span> <span data-ttu-id="8c2b6-242">Le gestionnaire d’événements **ready** effectue les quatre étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-242">The **ready** event handler does the following four steps:</span></span> 
    
    1. <span data-ttu-id="8c2b6-243">Initialise la variable globale **projContext** avec le contexte client pour le JSOM Project Server et la variable globale **pwaWeb**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-243">Initializes the **projContext** global variable with the client context for the Project Server JSOM and the **pwaWeb** global variable.</span></span> 
        
    2. <span data-ttu-id="8c2b6-244">Appelle la fonction **getUserInfo** pour initialiser la variable globale **projUser**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-244">Calls the **getUserInfo** function to initialize the **projUser** global variable.</span></span> 
        
    3. <span data-ttu-id="8c2b6-245">Appelle la fonction **getAssignments**, qui obtient les données d’affectation spécifiées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-245">Calls the **getAssignments** function, which gets specified assignment data for the user.</span></span> 
        
    4. <span data-ttu-id="8c2b6-246">Lie les gestionnaires d’événements Click à la case à cocher de l’en-tête de tableau, et aux cases à cocher de chaque ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-246">Binds click event handlers to the table header check box, and to the check boxes in each row of the table.</span></span> <span data-ttu-id="8c2b6-247">Les gestionnaires d’événements Click gèrent l’attribut **checked** des cases à cocher lorsque l’utilisateur active ou désactive une case à cocher dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-247">The click event handlers manage the **checked** attribute of the check boxes when the user selects or clears any check box in the table.</span></span> 
    
- <span data-ttu-id="8c2b6-248">Si la fonction **getAssignments** réussit, elle appelle la fonction **onGetAssignmentsSuccess**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-248">If the **getAssignments** function is successful, it calls the **onGetAssignmentsSuccess** function.</span></span> <span data-ttu-id="8c2b6-249">Cette fonction insère une ligne dans le tableau pour chaque affectation, initialise les contrôles HTML dans chaque ligne et initialise ensuite les propriétés du bouton inférieur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-249">That function inserts a row in the table for each assignment, initializes the HTML controls in each row, and then initializes the bottom button properties.</span></span> 
    
- <span data-ttu-id="8c2b6-250">Le gestionnaire d’événements **OnClick** pour le bouton de **mise à jour** appelle la fonction **updateAssignments** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-250">The **onClick** event handler for the **Update** button calls the **updateAssignments** function.</span></span> <span data-ttu-id="8c2b6-251">Cette fonction obtient la valeur de pourcentage achevé qui est appliquée à chaque affectation sélectionnée ; ou si la zone de texte pourcentage achevé est vide, la fonction obtient le pourcentage d’achèvement de chaque affectation sélectionnée dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-251">That function gets the percent complete value that is applied to each selected assignment; or if the percent complete text box is empty, the function gets the percent complete of each selected assignment in the table.</span></span> <span data-ttu-id="8c2b6-252">La fonction **updateAssignments** enregistre puis envoie les mises à jour d’État et écrit un message sur les résultats au bas de la page.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-252">The **updateAssignments** function then saves and submits the status updates and writes a message about the results to the bottom of the page.</span></span> 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a><span data-ttu-id="8c2b6-253">Procédure 3.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-253">Procedure 3.</span></span> <span data-ttu-id="8c2b6-254">Pour créer les fonctions JavaScript</span><span class="sxs-lookup"><span data-stu-id="8c2b6-254">To create the JavaScript functions</span></span>

1. <span data-ttu-id="8c2b6-255">Dans Visual Studio, ouvrez le fichier App.js, puis supprimez tout le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-255">In Visual Studio, open the App.js file, and then delete all the content in the file.</span></span>
    
2. <span data-ttu-id="8c2b6-256">Ajoutez le gestionnaire d’événements **ready** des variables globales et du document.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-256">Add the global variables and the document **ready** event handler.</span></span> <span data-ttu-id="8c2b6-257">L’objet **document** est accessible à l’aide d’une fonction jQuery.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-257">The **document** object is accessed by using a jQuery function.</span></span> 
    
   <span data-ttu-id="8c2b6-p142">Le gestionnaire d’événements Click pour les cases à cocher d’en-tête de tableau définit l’état activé des cases à cocher de ligne. Si toutes les cases à cocher de ligne sont sélectionnées, ou toutes désactivées, le gestionnaire d’événements Click pour les cases à cocher de ligne définit l’état activé de la case à cocher d’en-tête. Les gestionnaires d’événements Click définissent également le message de résultats au bas de la page sur une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p142">The click event handler for the table header check box sets the checked state of the row check boxes. If all of the row check boxes are selected or all are clear, the click event handler for the row check boxes sets the checked state of the header check box. The click event handlers also set the results message at the bottom of the page to an empty string.</span></span>
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. <span data-ttu-id="8c2b6-261">Ajoutez la fonction **getUserInfo**, qui appelle **onGetUserNameSuccess** si la requête s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-261">Add the **getUserInfo** function, which calls **onGetUserNameSuccess** if the query is successful.</span></span> <span data-ttu-id="8c2b6-262">La fonction **onGetUserNameSuccess** remplace le contenu du paragraphe **caption** par une légende de tableau qui inclut le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-262">The **onGetUserNameSuccess** function replaces the contents of the **caption** paragraph with a table caption that includes the user name.</span></span> 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. <span data-ttu-id="8c2b6-263">Ajoutez la fonction **getAssignments**, qui appelle **onGetAssignmentsSuccess** (voir l’étape 5) si la requête d’affectation a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-263">Add the **getAssignments** function, which calls **onGetAssignmentsSuccess** (see step 5) if the assignment query is successful.</span></span> <span data-ttu-id="8c2b6-264">L’option **Include** limite la requête pour renvoyer uniquement les champs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-264">The **Include** option limits the query to return only the fields specified.</span></span> 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. <span data-ttu-id="8c2b6-265">Ajoutez la fonction **onGetAssignmentsSuccess** , qui ajoute une ligne pour chaque affectation au tableau.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-265">Add the **onGetAssignmentsSuccess** function, which adds a row for each assignment to the table.</span></span> <span data-ttu-id="8c2b6-266">La variable **prevProjName** est utilisée pour déterminer si une ligne concerne un autre projet.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-266">The **prevProjName** variable is used to determine whether a row is for a different project.</span></span> <span data-ttu-id="8c2b6-267">Si c’est le cas, le nom du projet est affiché en caractères gras ; Si ce n’est pas le cas, le nom du projet est défini sur une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-267">If so, the project name is shown in a bold font; if not, the project name is set to an empty string.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-268">Le JSOM n’inclut pas les propriétés **TimeSpan** incluses par l’CSOM, telles que **ActualWorkTimeSpan**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-268">The JSOM does not include **TimeSpan** properties that the CSOM includes, such as **ActualWorkTimeSpan**.</span></span> <span data-ttu-id="8c2b6-269">En revanche, le JSOM utilise des propriétés concernant le nombre de millisecondes, telles que la propriété [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-269">Instead, the JSOM uses properties for the number of milliseconds, such as the [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) property.</span></span> <span data-ttu-id="8c2b6-270">La méthode permettant d’obtenir cette propriété **est\_Get actualWorkMilliseconds**, qui renvoie une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-270">The method to get that property is **get\_actualWorkMilliseconds**, which returns an integer value.</span></span> <span data-ttu-id="8c2b6-271">> la méthode **get_actualWork** renvoie une chaîne telle que « 3H ».</span><span class="sxs-lookup"><span data-stu-id="8c2b6-271">> The **get_actualWork** method returns a string such as "3h".</span></span> <span data-ttu-id="8c2b6-272">Vous pouvez utiliser n’importe quelle valeur dans l’application **QuickStatus**, mais affichez-la différemment.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-272">You could use either value in the **QuickStatus** app, but display it differently.</span></span> <span data-ttu-id="8c2b6-273">La requête d’affectations inclut les deux propriétés, pour que vous puissiez tester la valeur pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-273">The assignments query includes both properties, so you can test the value during debugging.</span></span> <span data-ttu-id="8c2b6-274">Si vous supprimez la variable **actualWork**, vous pouvez également supprimer la propriété **ActualWork** dans la requête d’affectations.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-274">If you remove the **actualWork** variable, you can also remove the **ActualWork** property in the assignments query.</span></span> 
  
   <span data-ttu-id="8c2b6-275">Enfin, la fonction **onGetAssignmentsSuccess** initialise le bouton **Mettre à jour** et le bouton **Actualiser** avec les gestionnaires d’événements Click.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-275">Finally, the **onGetAssignmentsSuccess** function initializes the **Update** button and the **Refresh** button with click event handlers.</span></span> <span data-ttu-id="8c2b6-276">La valeur de texte du bouton **Mettre à jour** peut également être définie dans le code HTML.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-276">The text value of the **Update** button could also be set in the HTML code.</span></span> 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. <span data-ttu-id="8c2b6-277">Ajoutez le gestionnaire d’événements Click **updateAssignments** pour le bouton **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-277">Add the **updateAssignments** click event handler for the **Update** button.</span></span> <span data-ttu-id="8c2b6-278">Lorsque l’utilisateur modifie la valeur de pourcentage achevé d’une tâche ou ajoute une valeur dans la zone de texte **percentComplete**, la valeur peut être saisie dans plusieurs formats tels que « 60 », « 60% » ou « 60 % ».</span><span class="sxs-lookup"><span data-stu-id="8c2b6-278">When the user changes a value for percent complete of a task, or adds a value in the **percentComplete** text box, the value could be entered in several formats such as "60", "60%", or "60 %".</span></span> <span data-ttu-id="8c2b6-279">La méthode **getNumericValue** renvoie la valeur numérique de la saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-279">The **getNumericValue** method returns the numeric value of the input text.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-280">Dans une application conçue pour une utilisation en production, les valeurs d’entrée pour les informations numériques doivent inclure une validation de champ et une vérification des erreurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-280">In an app that is designed for production use, input values for numeric information should include field validation and additional error checking.</span></span> 
  
   <span data-ttu-id="8c2b6-281">L’exemple **updateAssignments** inclut une vérification des erreurs de base et affiche les informations dans le paragraphe **message** au bas de la page : vert si la requête de mise à jour a réussi et rouge s’il existe une erreur d’entrée ou en cas d’échec de la requête de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-281">The **updateAssignments** example includes some basic error checking, and displays information in the **message** paragraph at the bottom of the page—green if the update query is successful and red if there is an input error or the update query is unsuccessful.</span></span> 
    
   <span data-ttu-id="8c2b6-282">Avant d’utiliser la méthode **submitAllStatusUpdates**, l’application doit enregistrer les mises à jour sur le serveur à l’aide de la méthode **PS.StatusAssignmentCollection.update**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-282">Before using the **submitAllStatusUpdates** method, the app must save the updates to the server by using the **PS.StatusAssignmentCollection.update** method.</span></span> 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. <span data-ttu-id="8c2b6-283">Ajoutez la fonction **exitToPwa** , qui utilise le paramètre de chaîne de requête **SPHOSTURL** pour l’URL du site Project Web App hôte.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-283">Add the **exitToPwa** function, which uses the **SPHostUrl** query string parameter for the URL of the host Project Web App site.</span></span> <span data-ttu-id="8c2b6-284">Pour revenir à la page tâches, ajoutez `"/Tasks.aspx"` à l’URL.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-284">To navigate back to the Tasks page, append  `"/Tasks.aspx"` to the URL.</span></span> <span data-ttu-id="8c2b6-285">Par exemple, la variable **spHostUrl** est définie sur `https://ServerName/ProjectServerName/Tasks.aspx`.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-285">For example, the **spHostUrl** variable would be set to  `https://ServerName/ProjectServerName/Tasks.aspx`.</span></span>
    
   <span data-ttu-id="8c2b6-286">La fonction **getQueryStringParameter** divise l’URL de la page **QuickStatus** pour extraire et renvoyer le paramètre spécifié dans les options de l’URL.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-286">The **getQueryStringParameter** function splits the URL of the **QuickStatus** page to extract and return the specified parameter in the URL options.</span></span> <span data-ttu-id="8c2b6-287">Voici un exemple de la valeur **document.URL** pour le document **QuickStatus** (tout sur une seule ligne) :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-287">Following is an example of the **document.URL** value for the **QuickStatus** document (all on one line):</span></span> 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   <span data-ttu-id="8c2b6-288">Pour l’URL précédente, la fonction **getQueryStringParameter** renvoie la valeur de la chaîne de `https://ServerName/pwa`requête **SPHostUrl** ,.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-288">For the previous URL, the **getQueryStringParameter** function returns the **SPHostUrl** query string value,  `https://ServerName/pwa`.</span></span> 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

<span data-ttu-id="8c2b6-289">Si vous publiez l’application **QuickStatus** à ce stade et que vous l’ajoutez à Project Web App, l’application peut être exécutée à partir de la page contenu du site, mais elle n’est pas facilement accessible aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-289">If you publish the **QuickStatus** app at this point and add it to Project Web App, the app can be run from the Site Contents page, but it is not easily available to users.</span></span> <span data-ttu-id="8c2b6-290">Pour aider les utilisateurs à trouver et à exécuter l’application, vous pouvez ajouter un bouton au niveau du ruban sur la page Tâches.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-290">To help users find and run the app, you can add a button for it to the ribbon on the Tasks page.</span></span> <span data-ttu-id="8c2b6-291">La procédure 4 explique comment ajouter une action personnalisée de ruban.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-291">Procedure 4 shows how to add a ribbon custom action.</span></span> 

<span data-ttu-id="8c2b6-292"><a name="pj15_StatusingApp_ribbon"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-292"><a name="pj15_StatusingApp_ribbon"> </a></span></span>

### <a name="adding-a-ribbon-custom-action"></a><span data-ttu-id="8c2b6-293">Ajout d’une action personnalisée du ruban</span><span class="sxs-lookup"><span data-stu-id="8c2b6-293">Adding a ribbon custom action</span></span>

<span data-ttu-id="8c2b6-294">Les onglets de ruban, les groupes et les contrôles pour Project Web App sont spécifiés dans le fichier pwaribbon. xml, `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` qui est installé dans le répertoire sur l’ordinateur exécutant Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-294">Ribbon tabs, groups, and controls for Project Web App are specified in the pwaribbon.xml file, which is installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directory on the computer running Project Server.</span></span> <span data-ttu-id="8c2b6-295">Pour vous aider à concevoir des actions personnalisées pour le ruban Project Web App, le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut une copie de pwaribbon. Xml.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-295">To help design custom actions for the Project Web App ribbon, the Project 2013 SDK download includes a copy of pwaribbon.xml.</span></span> 
  
<span data-ttu-id="8c2b6-296">Project Web App utilise des définitions de ruban différentes pour la page tâches, selon que l’instance de Project Web App utilise ou non le mode d’entrée unique qui permet aux utilisateurs d’entrer des valeurs pour la feuille de temps et l’état des tâches.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-296">Project Web App uses different ribbon definitions for the Tasks page, depending on whether the Project Web App instance uses single entry mode that enables users to enter values for both the timesheet and task status.</span></span> <span data-ttu-id="8c2b6-297">Si vous disposez d’autorisations d’administration pour Project Web App, pour déterminer le mode d’entrée, choisissez **paramètres PWA** dans le menu déroulant paramètres dans le coin supérieur droit de la page.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-297">If you have administrative permissions for Project Web App, to determine the entry mode, choose **PWA Settings** in the drop-down settings menu at the top-right corner of the page.</span></span> <span data-ttu-id="8c2b6-298">Sur la page Paramètres PWA, sélectionnez **Paramètres et valeurs par défaut de la feuille de temps**, puis observez la case à cocher **Mode d’entrée unique** en bas de la page.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-298">On the PWA Settings page, choose **Timesheet Settings and Defaults**, and then look at the **Single Entry Mode** check box at the bottom of the page.</span></span> 
  
<span data-ttu-id="8c2b6-299">Lorsque le mode d’entrée unique est désactivé, le ruban sur la page Tâches est défini par la région Mon travail dans pwaribbon.xml :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-299">When single entry mode is off, the ribbon on the Tasks page is defined by the My Work region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

<span data-ttu-id="8c2b6-300">Lorsque le mode d’entrée unique est activé, le ruban sur la page Tâches est défini par la région Mode lié dans pwaribbon.xml :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-300">When single entry mode is on, the Tasks page ribbon is defined by the Tied Mode region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

<span data-ttu-id="8c2b6-301">Bien que les groupes et les contrôles de chaque région se ressemblent, un contrôle du mode lié peut appeler une fonction différente de celle appelée par le même contrôle pour le mode non lié.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-301">Although the groups and controls in each region look similar, a control for the tied mode can call a different function than the same control for the non-tied mode.</span></span> <span data-ttu-id="8c2b6-302">La procédure 4 explique comment ajouter un contrôle de bouton pour l’application **QuickStatus** lorsque le mode d’entrée unique est désactivé (la case à cocher **Mode d’entrée unique** est désactivée).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-302">Procedure 4 shows how to add a button control for the **QuickStatus** app when single entry mode is off (the **Single Entry Mode** check box is clear).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8c2b6-303">Pour obtenir des informations générales sur l’ajout d’actions personnalisées à un ruban ou à un menu dans une application SharePoint, voir [créer des actions personnalisées à déployer avec les applications pour SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-303">For general information about adding custom actions to a ribbon or to a menu in a SharePoint application, see [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span></span> 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a><span data-ttu-id="8c2b6-304">Procédure 4.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-304">Procedure 4.</span></span> <span data-ttu-id="8c2b6-305">Pour ajouter une action personnalisée de ruban sur la page Tâches</span><span class="sxs-lookup"><span data-stu-id="8c2b6-305">To add a ribbon custom action to the Tasks page</span></span>

1. <span data-ttu-id="8c2b6-306">Examinez le ruban sur la page tâches dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-306">Examine the ribbon on the Tasks page in Project Web App.</span></span> <span data-ttu-id="8c2b6-307">Sélectionnez l’onglet **TÂCHES** dans le ruban et planifiez sa modification.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-307">Select the **TASKS** tab on the ribbon and plan how to modify it.</span></span> <span data-ttu-id="8c2b6-308">Il existe sept groupes, tels que **Envoyer**, **Tâches** et **Période**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-308">There are seven groups, such as **Submit**, **Tasks**, and **Period**.</span></span> <span data-ttu-id="8c2b6-309">Le groupe **Envoyer** a deux contrôles, un bouton **Enregistrer** et un menu déroulant **Envoyer l’état**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-309">The **Submit** group has two controls, a **Save** button and a **Send Status** drop-down menu.</span></span> <span data-ttu-id="8c2b6-310">Vous pouvez ajouter un contrôle à un emplacement quelconque dans un groupe, ajouter un groupe avec un nouveau contrôle à un emplacement quelconque dans l’onglet **TÂCHES** ou ajouter un autre onglet de ruban avec des groupes et contrôles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-310">You can add a control at any location in a group, add a group with a new control at any location in the **TASKS** tab, or add another ribbon tab that has custom groups and controls.</span></span> <span data-ttu-id="8c2b6-311">Dans cet exemple, nous ajoutons un troisième bouton au groupe **Envoyer**, où le bouton appelle l’URL de l’application **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-311">In this example, we add a third button to the **Submit** group, where the button invokes the URL of the **QuickStatus** app.</span></span> 
    
2. <span data-ttu-id="8c2b6-312">Dans le volet **Explorateur de solutions** dans Visual Studio, cliquez avec le bouton droit sur le projet **QuickStatus** et ajoutez un nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-312">In the **Solution Explorer** pane in Visual Studio, right-click the **QuickStatus** project, and then add a new item.</span></span> <span data-ttu-id="8c2b6-313">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Action personnalisée de ruban** (voir Figure 4).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-313">In the **Add New Item** dialog box, choose **Ribbon Custom Action** (see Figure 4).</span></span> <span data-ttu-id="8c2b6-314">Par exemple, nommez l’action personnalisée RibbonQuickStatusAction, puis choisissez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-314">For example, name the custom action RibbonQuickStatusAction, and then choose **Add**.</span></span>
    
   <span data-ttu-id="8c2b6-315">**Figure 4. Ajout d’une action personnalisée de ruban**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-315">**Figure 4. Adding a ribbon custom action**</span></span>

   <span data-ttu-id="8c2b6-316">![Ajout d’une action personnalisée du ruban](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Ajout d’une action personnalisée du ruban")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-316">![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")</span></span>
  
3. <span data-ttu-id="8c2b6-p158">Sur la première page de l’assistant **Créer une action personnalisée pour le Ruban**, maintenez l’option **Hôte web** sélectionnée, choisissez **Aucun** dans la liste déroulante pour l’étendue de l’action personnalisée, puis **Suivant** (voir figure 5). Les éléments des listes déroulantes sont pertinents pour SharePoint, et non pour Project Server. Nous remplacerons une grande partie du code XML généré pour l’action personnalisée afin qu’elle s’applique à Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p158">On the first page of the **Create Custom Action for Ribbon** wizard, leave the **Host Web** option selected, choose **None** in the drop-down list for the custom action scope, and then choose **Next** (see Figure 5). The items in the drop-down lists are relevant to SharePoint, not to Project Server. We will replace most of the generated XML for the custom action so that it applies to Project Server.</span></span> 
    
   <span data-ttu-id="8c2b6-320">**Figure 5. Définition des propriétés pour l’action personnalisée de ruban**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-320">**Figure 5. Specifying properties for the ribbon custom action**</span></span>

   <span data-ttu-id="8c2b6-321">![Définition des propriétés pour l’action personnalisée du ruban](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Définition des propriétés pour l’action personnalisée du ruban")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-321">![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")</span></span>
  
4. <span data-ttu-id="8c2b6-p159">Sur la page suivante de l’assistant **Créer une action personnalisée pour le Ruban**, maintenez toutes les valeurs par défaut pour les paramètres, puis sélectionnez **Terminer** (voir figure 6). Visual Studio crée le dossier **RibbonQuickStatusAction** qui contient un fichier Elements.xml.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p159">On the next page of the **Create Custom Action for Ribbon** wizard, leave all the default values for the settings, and then choose **Finish** (see Figure 6). Visual Studio creates the **RibbonQuickStatusAction** folder, which contains an Elements.xml file.</span></span> 
    
   <span data-ttu-id="8c2b6-324">**Figure 6. Définition des paramètres pour un contrôle de bouton**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-324">**Figure 6. Specifying the settings for a button control**</span></span>

   <span data-ttu-id="8c2b6-325">![Définition des paramètres pour un contrôle bouton](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Définition des paramètres pour un contrôle bouton")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-325">![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")</span></span>
  
5. <span data-ttu-id="8c2b6-326">Modifiez le code généré par défaut dans le fichier Elements.xml pour l’action personnalisée de ruban.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-326">Modify the default generated code in the Elements.xml file for the ribbon custom action.</span></span> <span data-ttu-id="8c2b6-327">Voici le code XML par défaut :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-327">Following is the default XML code:</span></span>
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. <span data-ttu-id="8c2b6-328">Dans l’élément **CustomAction**, supprimez l’attribut **Sequence** et l’attribut **Title**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-328">In the **CustomAction** element, delete the **Sequence** attribute and the **Title** attribute.</span></span> 
    
   2. <span data-ttu-id="8c2b6-329">Pour ajouter un contrôle au groupe d' **envoi** , recherchez le premier groupe dans la `Ribbon.ContextualTabs.MyWork.Home.Groups` collection dans le fichier pwaribbon. xml, qui est l’élément qui commence, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-329">To add a control to the **Submit** group, find the first group in the  `Ribbon.ContextualTabs.MyWork.Home.Groups` collection in the pwaribbon.xml file, which is the element that begins,  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span></span> <span data-ttu-id="8c2b6-330">Pour ajouter un contrôle enfant au groupe **Envoyer**, le code suivant illustre le bon attribut **Location** de l’élément **CommandUIDefinition** dans le fichier Elements.xml :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-330">To add a child control to the **Submit** group, the following code shows the correct **Location** attribute of the **CommandUIDefinition** element in the Elements.xml file:</span></span> 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. <span data-ttu-id="8c2b6-331">Modifier les valeurs d’attribut de l’élément enfant **Button** comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-331">Change the attribute values of the child **Button** element as follows:</span></span> 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - <span data-ttu-id="8c2b6-332">Pour faire du bouton le troisième contrôle dans le groupe, l’attribut **Sequence** peut être un nombre plus élevé que `Sequence="20"` la valeur du contrôle d' **État d’envoi** existant (qui est un élément **FlyoutAnchor** dans pwaribbon. Xml).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-332">To make the button the third control in the group, the **Sequence** attribute can be any number higher than the  `Sequence="20"` value of the existing **Send Status** control (which is a **FlyoutAnchor** element in pwaribbon.xml).</span></span> <span data-ttu-id="8c2b6-333">Par Convention, les numéros de séquence des groupes et des `10, 20, 30, …`contrôles sont, ce qui permet d’insérer des éléments dans des positions intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-333">By convention, the sequence numbers of groups and controls are  `10, 20, 30, …`, which enables elements to be inserted in intermediate positions.</span></span>
    
       - <span data-ttu-id="8c2b6-334">L’attribut **Command** spécifie la commande à exécuter dans l’élément **CommandUIHandler** (voir l’étape suivante, 5.d).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-334">The **Command** attribute specifies the command to run in the **CommandUIHandler** element (see the following step 5.d).</span></span> <span data-ttu-id="8c2b6-335">Vous pouvez simplifier le nom de commande pour aider le développeur suivant.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-335">You can simplify the command name to make it easier for the next developer.</span></span> <span data-ttu-id="8c2b6-336">Par exemple `Command="Invoke_QuickStatus"` , est plus facile à `Command="Invoke_RibbonQuickStatusActionButtonRequest"`lire que.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-336">For example  `Command="Invoke_QuickStatus"` is easier to read than  `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span></span>
    
       - <span data-ttu-id="8c2b6-337">Les attributs d’image spécifient l’icône 16 x 16 pixels et l’icône de 32 x 32 pixels pour le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-337">The image attributes specify the 16 x 16-pixel icon and the 32 x 32-pixel icon for the button control.</span></span> <span data-ttu-id="8c2b6-338">Dans le fichier Elements. xml par `Image32by32="_layouts/15/images/placeholder32x32.png"` défaut, spécifie un point orange.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-338">In the default Elements.xml file,  `Image32by32="_layouts/15/images/placeholder32x32.png"` specifies an orange dot.</span></span> <span data-ttu-id="8c2b6-339">Vous pouvez extraire des icônes des fichiers image map (ps16x16. png et ps32x32. png) qui sont installés dans le `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` répertoire sur l’ordinateur exécutant Project Server.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-339">You can extract icons from the image map files (ps16x16.png and ps32x32.png) that are installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directory on the computer running Project Server.</span></span> <span data-ttu-id="8c2b6-340">Par exemple, l’icône 32 x 32 pixels se trouve dans la deuxième colonne des icônes à partir de la gauche et la dixième ligne en bas à partir du haut de la ps32x32. png image map (la partie supérieure de l’icône se trouve après la neuvième ligne, 9 lignes x 32 pixels/Row = 288 pixels).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-340">For example, the 32 x 32-pixel icon is in the second column of icons from the left and the tenth row down from the top of the ps32x32.png image map (the top of the icon is after the end of the ninth row; 9 rows x 32 pixels/row = 288 pixels).</span></span> 
    
       - <span data-ttu-id="8c2b6-341">Pour afficher une info-bulle pour le contrôle de bouton, ajoutez l’attribut **ToolTipTitle** et l’attribut **ToolTipDescription**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-341">To show a tool tip for the button control, add the **ToolTipTitle** attribute and the **ToolTipDescription** attribute.</span></span> 
    
    4. <span data-ttu-id="8c2b6-342">Modifiez les attributs de l’élément **CommandUIHandler**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-342">Change the attributes of the **CommandUIHandler** element.</span></span> <span data-ttu-id="8c2b6-343">Par exemple, assurez-vous que l’attribut **Command** correspond à la valeur d’attribut **Command** de l’élément **Button**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-343">For example, ensure that the **Command** attribute matches the **Command** attribute value for the **Button** element.</span></span> <span data-ttu-id="8c2b6-344">Pour l’attribut **CommandAction** , `~appWebUrl` est un espace réservé pour l’URL de la page Web **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-344">For the **CommandAction** attribute,  `~appWebUrl` is a placeholder for the URL of the **QuickStatus** webpage.</span></span> <span data-ttu-id="8c2b6-345">Lorsque le bouton du ruban appelle l’application **QuickStatus**, le jeton **{StandardTokens}** est remplacé par les options d’URL qui incluent **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber** et **SPAppWebUrl**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-345">When the ribbon button invokes the **QuickStatus** app, the **{StandardTokens}** token is replaced by URL options that include **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**, and **SPAppWebUrl**.</span></span>
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. <span data-ttu-id="8c2b6-346">Dans l’**Explorateur de solutions**, ouvrez le concepteur **Feature1.feature**, puis déplacez l’élément **RibbonQuickStatusAction** du volet **Éléments dans la solution** vers le volet **Éléments dans la fonctionnalité**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-346">In **Solution Explorer**, open the **Feature1.feature** designer, and move the **RibbonQuickStatusAction** item from the **Items in the Solution** pane to the **Items in the Feature** pane.</span></span> <span data-ttu-id="8c2b6-347">Si vous ouvrez le concepteur **Package.package**, l’élément **RibbonQuickStatusAction** sera dans le volet **Éléments dans le package**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-347">If you then open the **Package.package** designer, the **RibbonQuickStatusAction** item will be in the **Items in the Package** pane.</span></span> 
    
<span data-ttu-id="8c2b6-348">Lors du développement de l’application et de l’ajout d’un bouton de ruban, vous testez généralement l’application et définissez des points d’arrêt dans le code JavaScript pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-348">As you develop the app and add a ribbon button, you normally test the app and set breakpoints in the JavaScript code for debugging.</span></span> <span data-ttu-id="8c2b6-349">Lorsque vous appuyez sur **F5** pour démarrer le débogage, Visual Studio compile l’application, la déploie sur le site spécifié dans la propriété **URL du site** du projet **QuickStatus** et affiche une page qui vous demande si vous faites confiance à l’application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-349">When you press **F5** to start debugging, Visual Studio compiles the app, deploys it to the site that is specified in the **Site URL** property of the **QuickStatus** project, and displays a page that asks whether you trust the app.</span></span> <span data-ttu-id="8c2b6-350">Lorsque vous continuez puis quittez l’application **QuickStatus** , elle revient à la page tâches dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-350">When you proceed and then exit the **QuickStatus** app, it returns to the Tasks page in Project Web App.</span></span> 

> [!NOTE]
> <span data-ttu-id="8c2b6-351">La figure 7 montre que le bouton **État rapide** sur l’onglet **TÂCHES** du ruban est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-351">Figure 7 shows that the **Quick Status** button on the **TASKS** tab of the ribbon is disabled.</span></span> <span data-ttu-id="8c2b6-352">Après plusieurs déploiements de débogage avec Visual Studio, des contrôles de ruban personnalisé peuvent être bloqués lorsque vous continuez à déboguer ou déployer l’application publiée sur le même serveur de test.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-352">After many debug deployments with Visual Studio, custom ribbon controls can be blocked when you continue to debug or deploy the published app on the same test server.</span></span> <span data-ttu-id="8c2b6-353">Pour activer le bouton, supprimez l’élément **RibbonQuickStatusAction** dans Visual Studio et créez une action de ruban avec un ID et un nom différents.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-353">To enable the button, delete the **RibbonQuickStatusAction** item in Visual Studio, and then create a new ribbon action that has a different name and ID.</span></span> <span data-ttu-id="8c2b6-354">Si cela ne résout pas le problème, essayez de supprimer l’application de l’instance de test de Project Web App, puis recréez l’application avec un ID d’application différent.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-354">If that doesn't solve the problem, try removing the app from the Project Web App test instance, and then recreate the app with a different app ID.</span></span> 
  
<span data-ttu-id="8c2b6-355">**Figure 7. Affichage de l’info-bulle du bouton État rapide désactivé**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-355">**Figure 7. Viewing the tooltip of the disabled Quick Status button**</span></span>

<span data-ttu-id="8c2b6-356">![Affichage de l’info-bulle du bouton désactivé](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Affichage de l’info-bulle du bouton désactivé")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-356">![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")</span></span>
  
<span data-ttu-id="8c2b6-357">La procédure 5 montre comment déployer et installer l’application **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-357">Procedure 5 shows how to deploy and install the **QuickStatus** app.</span></span> <span data-ttu-id="8c2b6-358">La procédure 6 présente quelques étapes supplémentaires pour le test de l’application, une fois celle-ci installée.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-358">Procedure 6 shows some additional steps in testing the app after you have installed it.</span></span> 

<span data-ttu-id="8c2b6-359"><a name="pj15_StatusingApp_Deploying"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-359"><a name="pj15_StatusingApp_Deploying"> </a></span></span>

## <a name="deploying-the-quickstatus-app"></a><span data-ttu-id="8c2b6-360">Déploiement de l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-360">Deploying the QuickStatus app</span></span>

<span data-ttu-id="8c2b6-361">Il existe plusieurs façons de déployer une application vers une application Web SharePoint telle que Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-361">There are several ways to deploy an app to a SharePoint web application such as Project Web App.</span></span> <span data-ttu-id="8c2b6-362">Le déploiement que vous utilisez dépend de la publication de l’application dans un catalogue SharePoint privé ou dans l’Office Store public, et si SharePoint est installé en local ou s’il s’agit d’un client en ligne.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-362">Which deployment you use will depend on whether you want to publish the app to a private SharePoint catalog or to the public Office Store, and whether SharePoint is installed on-premises or is an online tenancy.</span></span> <span data-ttu-id="8c2b6-363">La procédure 5 montre comment déployer l’application **QuickStatus** sur une installation locale dans un catalogue d’applications privé.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-363">Procedure 5 shows how to deploy the **QuickStatus** app to an on-premises installation in a private app catalog.</span></span> <span data-ttu-id="8c2b6-364">Pour plus d’informations, voir [installer et gérer des applications pour sharepoint 2013](https://technet.microsoft.com/library/fp161232.aspx) et [publier des applications pour SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c2b6-364">For more information, see [Install and manage apps for SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) and [Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span></span>
  
> [!NOTE]
> <span data-ttu-id="8c2b6-365">L’ajout d’une application à un catalogue SharePoint nécessite des autorisations d’administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-365">Adding an app to a SharePoint catalog requires SharePoint administrator permissions.</span></span> 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a><span data-ttu-id="8c2b6-p171">Procédure 5. Pour déployer l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p171">Procedure 5. To deploy the QuickStatus app</span></span>

1. <span data-ttu-id="8c2b6-368">Dans Visual Studio, enregistrez tous les fichiers, puis cliquez avec le bouton droit sur le projet **QuickStatus** dans l’**Explorateur de solutions** et choisissez **Publier**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-368">In Visual Studio, save all of the files, and then right-click the **QuickStatus** project in the **Solution Explorer** and choose **Publish**.</span></span>
    
2. <span data-ttu-id="8c2b6-369">Étant donné que l’application **QuickStatus** est hébergée par SharePoint, il existe très peu d’options de publication (voir la figure 8).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-369">Because the **QuickStatus** app is SharePoint-hosted, there are very few options for publishing (see Figure 8).</span></span> <span data-ttu-id="8c2b6-370">Dans la boîte de dialogue \*\* Publier des applications pour Office et SharePoint\*\*, choisissez \*\*Terminer \*\*.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-370">In the **Publish apps for Office and SharePoint** dialog box, choose **Finish**.</span></span>
    
   <span data-ttu-id="8c2b6-371">**Figure 8. Publication de l’application QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-371">**Figure 8. Publishing the QuickStatus app**</span></span>

   <span data-ttu-id="8c2b6-372">![Utilisation de l’Assistant Publication](media/pj15_CreateStatusingApp_PublishWizard.gif "Utilisation de l’Assistant Publication")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-372">![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")</span></span>
  
3. <span data-ttu-id="8c2b6-373">Copiez le fichier QuickStatus. app du `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` répertoire dans un répertoire pratique de l’ordinateur local (ou sur l’ordinateur SharePoint pour une installation locale).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-373">Copy the QuickStatus.app file from the  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directory to a convenient directory on the local computer (or to the SharePoint computer for an on-premises installation).</span></span> 
    
4. <span data-ttu-id="8c2b6-374">Dans l’Administration centrale de SharePoint, choisissez **Applications** dans la barre de lancement rapide, puis choisissez **Gérer le catalogue d’applications**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-374">In SharePoint Central Administration, choose **Apps** in the Quick Launch, and then choose **Manage App Catalog**.</span></span>
    
5. <span data-ttu-id="8c2b6-375">S’il n’existe pas de catalogue d’applications, créez une collection de sites pour le catalogue d’applications, en suivant la section *configurer le site de catalogue d’applications pour une application Web* dans [gérer le catalogue d’applications dans SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-375">If an app catalog does not exist, create a site collection for the app catalog, by following the  *Configure the App Catalog site for a web application*  section in [Manage the App Catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span></span>
    
   <span data-ttu-id="8c2b6-376">Si un catalogue d’applications existe, accédez à l’URL du site sur la page Gérer le catalogue applications.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-376">If an app catalog exists, navigate to the site URL on the Manage App Catalog page.</span></span> <span data-ttu-id="8c2b6-377">Par exemple, dans les étapes suivantes, le site de catalogue d' `https://ServerName/sites/TestApps`applications est.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-377">For example, in the following steps, the app catalog site is  `https://ServerName/sites/TestApps`.</span></span>
    
6. <span data-ttu-id="8c2b6-p174">Sur la page du catalogue d’applications, choisissez **Applications pour SharePoint** dans la barre de lancement rapide. Sur la page Applications pour SharePoint, sur l’onglet **FICHIERS** du ruban, choisissez **Télécharger un document**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p174">On the app catalog page, choose **Apps for SharePoint** in the Quick Launch. On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Upload Document**.</span></span>
    
7. <span data-ttu-id="8c2b6-380">Dans la boîte de dialogue **Ajouter un document**, recherchez le fichier QuickStatus.app, ajoutez des commentaires pour la version, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-380">In the **Add a document** dialog box, browse for the QuickStatus.app file, add comments for the version, and then choose **OK**.</span></span>
    
8. <span data-ttu-id="8c2b6-381">Lorsque vous ajoutez une application, vous pouvez également ajouter des informations locales pour la description de l’application, l’icône et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-381">When you add an app, you can also add local information for the app description, icon, and other information.</span></span> <span data-ttu-id="8c2b6-382">Dans la boîte de dialogue **Apps for SharePoint-QuickStatus. app** , ajoutez les informations que vous souhaitez afficher pour l’application dans la collection de sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-382">In the **Apps for SharePoint - QuickStatus.app** dialog box, add the information that you want to show for the app in the SharePoint site collection.</span></span> <span data-ttu-id="8c2b6-383">Par exemple, ajoutez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-383">For example, add the following information:</span></span> 
    
   1. <span data-ttu-id="8c2b6-384">Champ **description courte** : tapez application de test d’État rapide.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-384">**Short Description** field: Type Quick Status test app.</span></span>
    
   2. <span data-ttu-id="8c2b6-385">Champ **Description** : tapez application de test pour mettre à jour le pourcentage achevé des tâches dans plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-385">**Description** field: Type Test app to update percent complete for tasks in multiple projects.</span></span>
    
   3. <span data-ttu-id="8c2b6-386">Champs d' **URL d’icône** : ajoutez une image 96 x 96 pixels pour l’icône de l’application aux ressources de site du catalogue d’applications.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-386">**Icon URL** fields: Add a 96 x 96-pixel image for the app icon to the site assets for the app catalog.</span></span> <span data-ttu-id="8c2b6-387">Par exemple, accédez à `https://ServerName/sites/TestApps`, choisissez **contenu du site** dans le menu déroulant **paramètres** , choisissez **ressources de site**, puis ajoutez l’image quickStatusApp. png.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-387">For example, navigate to  `https://ServerName/sites/TestApps`, choose **Site contents** in the **Settings** drop-down menu, choose **Site Assets**, and then add the quickStatusApp.png image.</span></span> <span data-ttu-id="8c2b6-388">Cliquez avec le bouton droit sur l’élément **quickStatusApp**, choisissez **Propriétés**, puis copiez la valeur **Adresse (URL)** dans la boîte de dialogue **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-388">Right-click the **quickStatusApp** item, choose **Properties**, and then copy the **Address (URL)** value in the **Properties** dialog box.</span></span> <span data-ttu-id="8c2b6-389">Par exemple, copiez `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, puis collez la valeur dans le champ URL de l’URL de l' **icône** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-389">For example, copy  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, and then paste the value in the **Icon URL** web address field.</span></span> <span data-ttu-id="8c2b6-390">Saisissez une description de l’icône, par exemple (comme dans la figure 9) entrezIcône de l’application QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-390">Type a description for the icon, for example (as in Figure 9), type QuickStatus app icon.</span></span> <span data-ttu-id="8c2b6-391">Vérifiez la validité de l’URL.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-391">Test that the URL is valid.</span></span>
    
      <span data-ttu-id="8c2b6-392">**Figure 9. Ajout d’une URL d’icône pour l’application QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-392">**Figure 9. Adding an icon URL for the QuickStatus app**</span></span>

      <span data-ttu-id="8c2b6-393">![Définition des propriétés dans SharePoint pour l’application](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Définition des propriétés dans SharePoint pour l’application")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-393">![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")</span></span>
  
   4. <span data-ttu-id="8c2b6-394">Champ **Catégorie** : choisissez une catégorie existante ou spécifiez votre propre valeur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-394">**Category** field: Choose an existing category, or specify your own value.</span></span> <span data-ttu-id="8c2b6-395">Par exemple, saisissez État.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-395">For example, type Statusing.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="8c2b6-396">Une catégorie nommée **État** sert uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-396">A category named **Statusing** is just for testing purposes.</span></span> <span data-ttu-id="8c2b6-397">Une catégorie typique pour les applications de Project Server est **Gestion de projet**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-397">A typical category for Project Server apps is **Project Management**.</span></span> 
  
   5. <span data-ttu-id="8c2b6-398">Champ **Nom de l’éditeur** : saisissez le nom de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-398">**Publisher name** field: Type the name of the publisher.</span></span> <span data-ttu-id="8c2b6-399">Dans cet exemple, entrez Kit de développement logiciel (SDK) Project.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-399">In this example, type Project SDK.</span></span>
    
   6. <span data-ttu-id="8c2b6-400">Champ **activé** : pour que l’application soit visible par les administrateurs de site Project Web App, activez la case à cocher **activé** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-400">**Enabled** field: To make the app visible to Project Web App site administrators for installation, select the **Enabled** check box.</span></span> 
    
   7. <span data-ttu-id="8c2b6-p180">Les champs supplémentaires sont facultatifs. Par exemple, vous pouvez ajouter une URL de support technique et plusieurs images d’aide pour la page de détails d’application. Dans la figure 9, les champs **URL d’image 1** incluent l’URL de la capture d’écran de l’application et une description de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-p180">Additional fields are optional. For example, you can add a support URL and multiple help images for the app details page. In Figure 9, the **Image URL 1** fields include the URL for a screenshot of the app and a description of the screenshot.</span></span> 
    
   8. <span data-ttu-id="8c2b6-404">Dans la boîte de dialogue **applications pour SharePoint-QuickStatus. app** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-404">In the **Apps for SharePoint - QuickStatus.app** dialog box, choose **Save**.</span></span> <span data-ttu-id="8c2b6-405">Dans la figure 9, l’élément **mise à jour de l’État rapide** de la bibliothèque apps pour SharePoint est extrait pour modification, ainsi, sous l’onglet **modifier** du ruban de la boîte de dialogue, vous choisirez **Archiver** pour terminer le processus (voir figure 10).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-405">In Figure 9, the **Quick Status Update** item in the Apps for SharePoint library is checked out for editing, so on the **EDIT** tab of the dialog box ribbon, you would choose **Check In** to complete the process (see Figure 10).</span></span> 
    
      <span data-ttu-id="8c2b6-406">**Figure 10. L’application QuickStatus est ajoutée dans la bibliothèque Applications pour SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-406">**Figure 10. The QuickStatus app is added to the Apps for SharePoint library.**</span></span>

      <span data-ttu-id="8c2b6-407">![L’application QuickStatus est ajoutée à SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "L’application QuickStatus est ajoutée à SharePoint")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-407">![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")</span></span>
  
9. <span data-ttu-id="8c2b6-408">Dans Project Web App, dans le menu déroulant **paramètres** , choisissez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-408">In Project Web App, in the **Settings** drop-down menu, choose **Add an app**.</span></span> <span data-ttu-id="8c2b6-409">Sur la page Vos applications, dans la barre de lancement rapide, choisissez **De votre organisation**, puis **Détails de l’application** pour l’application **Mise à jour de l’état rapide**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-409">On the Your Apps page, in the Quick Launch, choose **From Your Organization**, and then choose **App Details** for the **Quick Status Update** app.</span></span> <span data-ttu-id="8c2b6-410">La figure 11 montre la page de détails avec l’icône d’application, la capture d’écran et les informations que vous avez ajoutées à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-410">Figure 11 shows the details page with the app icon, screenshot, and other information that you added in the previous step.</span></span> 
    
   <span data-ttu-id="8c2b6-411">**Figure 11. Utilisation de la page de détails Mise à jour de l’état rapide dans Project Web App**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-411">**Figure 11. Using the Quick Status Update details page in Project Web App**</span></span>

   <span data-ttu-id="8c2b6-412">![Ajout de l’application QuickStatus à Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Ajout de l’application QuickStatus à Project Web App")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-412">![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")</span></span>
  
10. <span data-ttu-id="8c2b6-413">Sur la page de détails Mise à jour de l’état rapide, choisissez **AJOUTER**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-413">On the Quick Status Update details page, choose **ADD IT**.</span></span> <span data-ttu-id="8c2b6-414">Project Web App affiche une boîte de dialogue qui répertorie les opérations que l’application QuickStatus peut effectuer (voir figure 12).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-414">Project Web App displays a dialog box that lists the operations that the QuickStatus app can perform (see Figure 12).</span></span> <span data-ttu-id="8c2b6-415">La liste des opérations est dérivée des éléments **AppPermissionRequest** du fichier AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-415">The list of operations is derived from the **AppPermissionRequest** elements in the AppManifest.xml file.</span></span> 
    
    <span data-ttu-id="8c2b6-416">**Figure 12. Vérification de la confiance accordée à l’application QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-416">**Figure 12. Verifying that you trust the Quick Status app**</span></span>

    <span data-ttu-id="8c2b6-417">![Vérification de l’approbation pour l’application QuickStatus](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Vérification de l’approbation pour l’application QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-417">![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")</span></span>
  
11. <span data-ttu-id="8c2b6-418">Dans la boîte de dialogue **Faites-vous confiance à la mise à jour de l’état rapide ?**, choisissez **Approuver**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-418">In the **Do you trust Quick Status Update** dialog box, choose **Trust It**.</span></span> <span data-ttu-id="8c2b6-419">L’application est ajoutée à la page contenu du site Project Web App (voir figure 13).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-419">The app is added to the Project Web App Site Contents page (see Figure 13).</span></span>
    
    <span data-ttu-id="8c2b6-420">**Figure 13. Affichage de l’application QuickStatus sur la page Contenu du site**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-420">**Figure 13. Viewing the Quick Status app on the Site Contents page**</span></span>

    <span data-ttu-id="8c2b6-421">![Affichage de l’application QuickStatus dans le contenu du site](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Affichage de l’application QuickStatus dans le contenu du site")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-421">![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")</span></span>
  
<span data-ttu-id="8c2b6-422">Sur la page Contenu du site, vous pouvez sélectionner l’icône **Mise à jour de l’état rapide** pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-422">On the Site Contents page, you can select the **Quick Status Update** icon to run the app.</span></span>

> [!NOTE]
> <span data-ttu-id="8c2b6-423">Pour les commandes supplémentaires qui fournissent des informations sur l’application, sur la page contenu du site, choisissez la zone qui contient le nom de la **mise à jour de l’État rapide** et les points de suspension (...). Vous pouvez consulter la page à propos de pour l’application, afficher la page des détails de l’application qui contient des informations sur les erreurs d’application, passer en revue la page des autorisations de l’application ou supprimer l’application de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-423">For additional commands that provide information about the app, on the Site Contents page, choose the region that contains the **Quick Status Update** name and the ellipsis (...). You can review the About page for the app, view the App Details page that contains information about app errors, review the app permissions page, or remove the app from Project Web App.</span></span> 
  
<span data-ttu-id="8c2b6-424">Sur la page tâches de Project Web App (voir figure 14), le bouton **QuickStatus** doit être activé sur le ruban.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-424">On the Tasks page in Project Web App (see Figure 14), the **QuickStatus** button should be enabled on the ribbon.</span></span> <span data-ttu-id="8c2b6-425">Si le bouton **État rapide** est désactivé, essayez les actions décrites dans la remarque de la figure 7.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-425">If the **Quick Status** button is disabled, try the actions described in the note for Figure 7.</span></span> 

<span data-ttu-id="8c2b6-426">**Figure 14. Lancement de l’application QuickStatus à partir de l’onglet TÂCHES**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-426">**Figure 14. Starting the QuickStatus app from the TASKS tab**</span></span>

<span data-ttu-id="8c2b6-427">![Lancement de l’application QuickStatus à partir de l’onglet TÂCHES](media/pj15_CreateStatusingApp_TasksRibbon.gif "Lancement de l’application QuickStatus à partir de l’onglet TÂCHES")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-427">![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")</span></span>
  
<span data-ttu-id="8c2b6-428">La procédure 6 décrit certains tests à effectuer avec l’application QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-428">Procedure 6 shows some tests to make with the QuickStatus app.</span></span>

<span data-ttu-id="8c2b6-429"><a name="pj15_StatusingApp_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-429"><a name="pj15_StatusingApp_Testing"> </a></span></span>

## <a name="testing-the-quickstatus-app"></a><span data-ttu-id="8c2b6-430">Test de l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-430">Testing the QuickStatus app</span></span>

<span data-ttu-id="8c2b6-431">Chaque opération qu’un utilisateur peut essayer dans l’application **QuickStatus** doit être testée sur une installation de test de Project Server avant de déployer l’application sur un serveur de production ou sur un client de production de Project online.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-431">Every operation that a user might try in the **QuickStatus** app should be tested on a test installation of Project Server before deploying the app to a production server or to a production tenant of Project Online.</span></span> <span data-ttu-id="8c2b6-432">Une installation de test vous permet de modifier et supprimer les affectations pour les utilisateurs sans répercussion aucune sur les projets réels.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-432">A test installation enables you to change and delete assignments for users without affecting actual projects.</span></span> <span data-ttu-id="8c2b6-433">Le test doit également impliquer plusieurs utilisateurs ayant différents ensembles d’autorisations, comme un administrateur, un responsable de projet et un membre d’équipe.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-433">Testing should also involve several users who have different sets of permissions, such as administrator, project manager, and team member.</span></span> <span data-ttu-id="8c2b6-434">Des tests minutieux peuvent révéler des modifications devant être effectuées dans l’application, qui n’ont pas été repérées lors du test effectué pendant le développement.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-434">Thorough testing can uncover changes that should be made in the app, which were not apparent in testing during development.</span></span> <span data-ttu-id="8c2b6-435">La procédure 6 répertorie plusieurs tests pour l’application **QuickStatus**, cette série de tests n’est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-435">Procedure 6 lists several tests for the **QuickStatus** app, but does not include an exhaustive series of tests.</span></span> 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a><span data-ttu-id="8c2b6-436">Procédure 6.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-436">Procedure 6.</span></span> <span data-ttu-id="8c2b6-437">Pour tester l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-437">To test the QuickStatus app</span></span>

1. <span data-ttu-id="8c2b6-438">Exécutez l’application **QuickStatus** sur laquelle l’utilisateur n’a aucune affectation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-438">Run the **QuickStatus** app where the user has no assignments.</span></span> <span data-ttu-id="8c2b6-439">L’application doit afficher un message bleu en bas de la page, par exemple, **Le nom d’utilisateur ne dispose d’aucune affectation**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-439">The app should show a blue message at the bottom of the page, for example, **User Name has no assignments**.</span></span>
    
   <span data-ttu-id="8c2b6-440">Choisissez **Mettre à jour**. Le message devient alors vert et indique **Les affectations ont été mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-440">Choose **Update**, and the message changes to a green **Assignments have been updated**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8c2b6-441">Le comportement de l’application doit être modifié de sorte que le bouton **mettre à jour** soit désactivé lorsqu’il n’y a aucune affectation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-441">The app behavior should be changed so that the **Update** button is disabled when there are no assignments.</span></span> 
  
2. <span data-ttu-id="8c2b6-442">Exécutez l’application dans laquelle l’utilisateur dispose de plusieurs affectations dans différents projets et que certaines affectations ne sont pas terminées.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-442">Run the app where the user has multiple assignments in several different projects and some assignments are not complete.</span></span> <span data-ttu-id="8c2b6-443">Notez l’apparence de l’application et effectuez les actions suivantes (voir figure 15) :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-443">Notice the appearance of the app and perform actions as follows (see Figure 15):</span></span>
    
   1. <span data-ttu-id="8c2b6-444">La fonction **onGetAssignmentsSuccess** crée une ligne dans le tableau pour chaque affectation de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-444">The **onGetAssignmentsSuccess** function creates a row in the table for each assignment for the current user.</span></span> <span data-ttu-id="8c2b6-445">Le nom du projet n’apparaît qu’une seule fois, dans une police de caractères gras, pour la première affectation de chaque projet.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-445">The project name shows only once, in a bold font, for the first assignment in each project.</span></span> 
    
   2. <span data-ttu-id="8c2b6-446">Désactivez la case à cocher dans l’en-tête de colonne nom de la **tâche** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-446">Clear the check box in the **Task name** column header.</span></span> <span data-ttu-id="8c2b6-447">Le gestionnaire d’événements Click de l’en-tête de tableau efface toutes les autres cases à cocher dans les lignes de tâche.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-447">The table header click event handler clears all of the other check boxes in the task rows.</span></span> 
    
   3. <span data-ttu-id="8c2b6-448">Sélectionnez toutes les tâches.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-448">Select all of the tasks.</span></span> <span data-ttu-id="8c2b6-449">Le gestionnaire d’événements Click de chaque ligne détermine si toutes les lignes sont sélectionnées et, si tel est le cas, sélectionne l’en-tête de colonne nom de la **tâche** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-449">The click event handler for each row determines whether all rows are selected, and if so, selects the **Task name** column header.</span></span> 
    
   4. <span data-ttu-id="8c2b6-450">Désactivez toutes les cases à cocher, puis sélectionnez une affectation qui a du travail restant.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-450">Clear all of the check boxes again, and then select one assignment that has some remaining work.</span></span> <span data-ttu-id="8c2b6-451">Par exemple, la figure 15 illustre la première tâche T1 a 20% de travail restant à effectuer.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-451">For example, Figure 15 shows the top task T1 has 20% remaining work to complete.</span></span>
    
   5. <span data-ttu-id="8c2b6-452">Dans la zone de texte **définir le pourcentage achevé** , tapez 80, puis choisissez **mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-452">In the **Set percent complete** text box, type 80, and then choose **Update**.</span></span> <span data-ttu-id="8c2b6-453">Le bas de la page doit afficher un message vert, les **affectations ont été mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-453">The bottom of the page should show a green message, **Assignments have been updated**.</span></span>
    
      <span data-ttu-id="8c2b6-454">**Figure 15. Mise à jour d’une affectation dans l’application QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-454">**Figure 15. Updating an assignment in the QuickStatus app**</span></span>

      <span data-ttu-id="8c2b6-455">![Mise à jour d’une affectation dans l’application QuickStatus](media/pj15_CreateStatusingApp_Testing1Update.gif "Mise à jour d’une affectation dans l’application QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-455">![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")</span></span>
  
3. <span data-ttu-id="8c2b6-456">Sélectionnez **Refresh** (reportez-vous à la figure 16).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-456">Choose **Refresh** (see Figure 16).</span></span> <span data-ttu-id="8c2b6-457">Toutes les tâches sont à nouveau sélectionnées, et la première tâche indique 80% achevé.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-457">All of the tasks are selected again, and the top task shows 80% complete.</span></span> 
    
      <span data-ttu-id="8c2b6-458">**Figure 16. Actualisation de la page de mise à jour d’État rapide**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-458">**Figure 16. Refreshing the Quick Status Update page**</span></span>

      <span data-ttu-id="8c2b6-459">![Actualisation de la page QuickStatus](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Actualisation de la page QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-459">![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")</span></span>
  
4. <span data-ttu-id="8c2b6-460">Désactivez toutes les cases à cocher, puis sélectionnez une autre tâche.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-460">Clear all of the check boxes, and then select another task.</span></span> <span data-ttu-id="8c2b6-461">Par exemple, sélectionnez **nouvelle tâche à partir de PWA**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-461">For example, select **New task from PWA**.</span></span> <span data-ttu-id="8c2b6-462">Laissez la zone de texte **définir le pourcentage achevé** vide, supprimez tout le texte de la colonne **% achevé** pour la tâche sélectionnée, puis choisissez **mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-462">Leave the **Set percent complete** text box empty, delete all text in the **% complete** column for the selected task, and then choose **Update**.</span></span> <span data-ttu-id="8c2b6-463">Étant donné que les deux zones de texte sont vides, l’application affiche un message d’erreur rouge (voir figure 17).</span><span class="sxs-lookup"><span data-stu-id="8c2b6-463">Because both text boxes are empty, the app shows a red error message (see Figure 17).</span></span>
    
      <span data-ttu-id="8c2b6-464">**Figure 17. Test du message d’erreur**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-464">**Figure 17. Testing the error message**</span></span>

      <span data-ttu-id="8c2b6-465">![Test du message d’erreur](media/pj15_CreateStatusingApp_Testing3Error.gif "Test du message d’erreur")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-465">![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")</span></span>
  
5. <span data-ttu-id="8c2b6-466">Mettez à jour la tâche précédente à 80% terminé, puis cliquez sur **quitter**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-466">Update the previous task to 80% complete, and then choose **Exit**.</span></span> <span data-ttu-id="8c2b6-467">La fonction **exitToPwa** remplace l’emplacement de la fenêtre du navigateur par la page tâches dans l’application hôte SharePoint (c’est-à-dire, l’URL https://ServerName/pwa/Tasks.aspx)devient.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-467">The **exitToPwa** function changes the browser window location to the Tasks page in the SharePoint host application (that is, the URL changes to https://ServerName/pwa/Tasks.aspx).</span></span> <span data-ttu-id="8c2b6-468">La figure 18 indique que la tâche **T1** et la tâche **New de** la tâche PWA indiquent 80% achevé.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-468">Figure 18 shows that the **T1** task and the **New task from PWA** task each show 80% complete.</span></span> 
    
      <span data-ttu-id="8c2b6-469">**Figure 18. Vérification de la mise à jour des tâches dans Project Web App**</span><span class="sxs-lookup"><span data-stu-id="8c2b6-469">**Figure 18. Verifying the tasks are updated in Project Web App**</span></span>

      <span data-ttu-id="8c2b6-470">![Vérification des tâches de mises à jour dans Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Vérification des tâches de mises à jour dans Project Web App")</span><span class="sxs-lookup"><span data-stu-id="8c2b6-470">![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")</span></span>
  
6. <span data-ttu-id="8c2b6-471">Avant que l’État mis à jour ne s’affiche dans Project Professional 2013, les modifications doivent être envoyées pour approbation, puis approuvées par le responsable de projet.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-471">Before the updated status shows in Project Professional 2013, the changes must be submitted for approval, and then approved by the project manager.</span></span>
    
<span data-ttu-id="8c2b6-472">Le test révèle plusieurs autres modifications qui doivent être apportées dans l’application **QuickStatus** pour une meilleure convivialité.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-472">Testing reveals several other changes that should be made in the **QuickStatus** app for improved usability.</span></span> <span data-ttu-id="8c2b6-473">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-473">For example:</span></span>

- <span data-ttu-id="8c2b6-474">Des contrôles d’erreur et une validation supplémentaires des valeurs de zone de texte devraient exister.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-474">There should be additional error checks and validation of text box values.</span></span> <span data-ttu-id="8c2b6-475">Actuellement, un utilisateur peut entrer une valeur non numérique ou une valeur négative pour le pourcentage achevé, ce qui entraîne un message d’erreur de type unfriendly.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-475">Currently, a user can enter a non-numeric value or a negative value for percent complete, which results in an unfriendly error message.</span></span> <span data-ttu-id="8c2b6-476">Par exemple, avec une valeur négative, le message d’erreur est une **erreur lors de la mise à jour des affectations : PJClientCallableException : StatusingSetDataValueInvalid**.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-476">For example, with a negative value, the error message is **Error updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.</span></span>
    
- <span data-ttu-id="8c2b6-477">Le message d’erreur pour les zones de texte vides peut répertorier le projet et la tâche, en plus du numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-477">The error message for blank text boxes could list the project and task, in addition to the row number.</span></span>
    
- <span data-ttu-id="8c2b6-478">Le message de réussite peut inclure une liste des tâches mises à jour ; Si la fonction **updateAssignments** réussit, elle peut effectuer une actualisation automatique de page et afficher les tâches ou les pourcentages mis à jour dans une couleur et une police en gras différentes.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-478">The success message could include a list of the tasks updated; or if the **updateAssignments** function is successful, it could perform an automatic page refresh and show updated tasks or percentages in a different color and bold font.</span></span> 
    
- <span data-ttu-id="8c2b6-479">Pour éviter une table très volumineuse, le tableau des affectations doit être limité aux tâches dont la taille est inférieure à 100%.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-479">To avoid a very large table, the table of assignments should be limited to tasks that are less than 100% complete.</span></span> <span data-ttu-id="8c2b6-480">Vous pouvez également ajouter une option pour afficher toutes les tâches.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-480">Or, add an option to show all tasks.</span></span> <span data-ttu-id="8c2b6-481">Ce problème peut également être résolu à l’aide d’une grille jQuery au lieu d’un tableau, où vous pouvez facilement implémenter le filtrage et la pagination de grille.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-481">This problem could also be solved by using a jQuery-based grid instead of a table, where you can easily implement filtering and grid paging.</span></span>
    
- <span data-ttu-id="8c2b6-482">Étant donné que l’application **QuickStatus** n’envoie pas d’État, l’icône d' **État rapide** sous l’onglet **tâches** du ruban sera plus logiquement la première icône du groupe **tâches** , et non la dernière icône du groupe d' **envoi** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-482">Because the **QuickStatus** app does not submit status, the **Quick Status** icon on the **TASKS** tab of the ribbon would more logically be the first icon in the **Tasks** group, rather than the last icon in the **Submit** group.</span></span> 
    
- <span data-ttu-id="8c2b6-483">Étant donné que la fonction **onGetAssignmentsSuccess** Initialise le texte du bouton **btnSubmitUpdate** , mais que les autres valeurs de texte de bouton sont initialisées en HTML, la page reste en état partiellement initialisé pendant l’exécution de la fonction **getAssignments** .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-483">Because the **onGetAssignmentsSuccess** function initializes the **btnSubmitUpdate** button text, but the other button text values are initialized in HTML, the page is left in a partially initialized state while the **getAssignments** function runs.</span></span> <span data-ttu-id="8c2b6-484">Les boutons de la page semblent plus cohérents si les valeurs de texte étaient toutes initialisées au format HTML.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-484">Buttons on the page would appear more consistent if the text values were all initialized in HTML.</span></span> 
    
<span data-ttu-id="8c2b6-485">Plus important encore, l’approche utilisée par l’application **QuickStatus** , dans laquelle elle modifie le pourcentage d’achèvement des affectations, doit être révisée dans une application de production.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-485">Most importantly, the approach that the **QuickStatus** app uses, where it changes percent complete for assignments, should be revised in a production app.</span></span> <span data-ttu-id="8c2b6-486">Pour plus d’informations, consultez la section [étapes suivantes](#pj15_StatusingApp_NextSteps) .</span><span class="sxs-lookup"><span data-stu-id="8c2b6-486">For more information, see the [Next steps](#pj15_StatusingApp_NextSteps) section.</span></span> 

<span data-ttu-id="8c2b6-487"><a name="pj15_StatusingApp_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-487"><a name="pj15_StatusingApp_Example"> </a></span></span>

## <a name="example-code-for-the-quickstatus-app"></a><span data-ttu-id="8c2b6-488">Exemple de code pour l’application QuickStatus</span><span class="sxs-lookup"><span data-stu-id="8c2b6-488">Example code for the QuickStatus app</span></span>

### <a name="defaultaspx-file"></a><span data-ttu-id="8c2b6-489">Fichier default. aspx</span><span class="sxs-lookup"><span data-stu-id="8c2b6-489">Default.aspx file</span></span>

<span data-ttu-id="8c2b6-490">Le code suivant se trouve dans `Pages\Default.aspx` le fichier du projet **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-490">The following code is in the  `Pages\Default.aspx` file of the **QuickStatus** project:</span></span> 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a><span data-ttu-id="8c2b6-491">Fichier app. js</span><span class="sxs-lookup"><span data-stu-id="8c2b6-491">App.js file</span></span>

<span data-ttu-id="8c2b6-492">Le code suivant se trouve dans `Scripts\App.js` le fichier du projet **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-492">The following code is in the  `Scripts\App.js` file of the **QuickStatus** project:</span></span> 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a><span data-ttu-id="8c2b6-493">Fichier App.css</span><span class="sxs-lookup"><span data-stu-id="8c2b6-493">App.css file</span></span>

<span data-ttu-id="8c2b6-494">Le code CSS suivant se trouve dans `Content\App.css` le fichier du projet **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-494">The following CSS code is in the  `Content\App.css` file of the **QuickStatus** project:</span></span> 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a><span data-ttu-id="8c2b6-495">Fichier Elements. xml pour le ruban</span><span class="sxs-lookup"><span data-stu-id="8c2b6-495">Elements.xml file for the ribbon</span></span>

<span data-ttu-id="8c2b6-496">La définition XML suivante, pour le bouton ajouter de l’onglet **tâches** sur le ruban, se trouve dans `RibbonQuickStatusAction\Elements.xml` le fichier du projet **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-496">The following XML definition, for the added button on the **TASKS** tab on the ribbon, is in the  `RibbonQuickStatusAction\Elements.xml` file of the **QuickStatus** project:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a><span data-ttu-id="8c2b6-497">Fichier AppManifest. Xml</span><span class="sxs-lookup"><span data-stu-id="8c2b6-497">AppManifest.xml file</span></span>

<span data-ttu-id="8c2b6-498">Voici le code XML pour le manifeste d’application du projet **QuickStatus** , qui inclut les deux étendues de demande d’autorisation nécessaires à la mise à jour de l’état de l’affectation de l’utilisateur de l’application dans plusieurs projets :</span><span class="sxs-lookup"><span data-stu-id="8c2b6-498">Following is the XML for the app manifest of the **QuickStatus** project, which includes the two permission request scopes that are necessary for updating the app user's assignment status in multiple projects:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a><span data-ttu-id="8c2b6-499">AppIcon. png, fichier</span><span class="sxs-lookup"><span data-stu-id="8c2b6-499">AppIcon.png file</span></span>

<span data-ttu-id="8c2b6-500">La solution Visual Studio complète pour l’application **QuickStatus** inclut un fichier personnalisé AppIcon. png.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-500">The complete Visual Studio solution for the **QuickStatus** app includes a custom AppIcon.png file.</span></span> <span data-ttu-id="8c2b6-501">La solution sera incluse dans le téléchargement du kit de développement logiciel (SDK) Project 2013.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-501">The solution will be included in the Project 2013 SDK download.</span></span> 

<span data-ttu-id="8c2b6-502"><a name="pj15_StatusingApp_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-502"><a name="pj15_StatusingApp_NextSteps"> </a></span></span>

## <a name="next-steps"></a><span data-ttu-id="8c2b6-503">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8c2b6-503">Next steps</span></span>

<span data-ttu-id="8c2b6-504">L’application **QuickStatus** est un exemple relativement simple qui explique comment écrire des applications qui peuvent être installées sur project Server 2013 et Project online.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-504">The **QuickStatus** app is a relatively simple example of how to write apps that can be installed on Project Server 2013 and Project Online.</span></span> <span data-ttu-id="8c2b6-505">La section [test de l’application QuickStatus](#pj15_StatusingApp_Testing) répertorie plusieurs améliorations pouvant être apportées pour une meilleure utilisation.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-505">The [Testing the QuickStatus app](#pj15_StatusingApp_Testing) section lists several improvements that can be made for better usability.</span></span> <span data-ttu-id="8c2b6-506">L’application **QuickStatus** utilise des fonctions JavaScript pour mettre à jour l’état des affectations pour Project Web App.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-506">The **QuickStatus** app uses JavaScript functions to update assignment status for Project Web App.</span></span> <span data-ttu-id="8c2b6-507">Toutefois, la modification du pourcentage d’achèvement de l’affectation n’est pas une pratique recommandée pour la gestion de projet.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-507">But, changing the assignment percent complete is not a recommended project management practice.</span></span> <span data-ttu-id="8c2b6-508">Une autre approche consiste à mettre à jour la date de début réelle et la durée restante des tâches affectées.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-508">Another approach would be to update the actual start date and remaining duration of assigned tasks.</span></span> <span data-ttu-id="8c2b6-509">Pour plus d’informations sur les problèmes, consultez la rubrique [mise à jour plus](https://www.mpug.com/articles/update-better) en détail dans le bulletin d’informations MPUG.</span><span class="sxs-lookup"><span data-stu-id="8c2b6-509">For a discussion of the issues, see [Update Better](https://www.mpug.com/articles/update-better) in the MPUG newsletter.</span></span> 

<span data-ttu-id="8c2b6-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="8c2b6-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="8c2b6-511">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2b6-511">See also</span></span>

- [<span data-ttu-id="8c2b6-512">Tâches de programmation Project Server</span><span class="sxs-lookup"><span data-stu-id="8c2b6-512">Project Server programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="8c2b6-513">Compléments SharePoint</span><span class="sxs-lookup"><span data-stu-id="8c2b6-513">SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163230.aspx)
- [<span data-ttu-id="8c2b6-514">Gestion des mises à jour de tâches dans Project Web App</span><span class="sxs-lookup"><span data-stu-id="8c2b6-514">Managing task updates in Project Web App</span></span>](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [<span data-ttu-id="8c2b6-515">Créer des actions personnalisées à déployer avec les compléments SharePoint</span><span class="sxs-lookup"><span data-stu-id="8c2b6-515">Create custom actions to deploy with SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163954.aspx)
    

