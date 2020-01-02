---
title: Développement d’une application Microsoft Project Online à l’aide du modèle objet côté client
manager: lindalu
ms.date: 12/18/2019
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: 'Cet article décrit le développement d’applications Microsoft Project Online à l’aide de .NET Framework 4.0 et CSOM. '
localization_priority: Priority
ms.openlocfilehash: 33ddafe2e3a75039bf55381524accf1a25692885
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825771"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model-csom"></a><span data-ttu-id="0a09b-103">Développement d’une application Microsoft Project Online à l’aide du modèle objet côté client (CSOM)</span><span class="sxs-lookup"><span data-stu-id="0a09b-103">Developing a Project Online application using the client-side object model</span></span>

>[!NOTE] 
><span data-ttu-id="0a09b-104">Cet article décrit le développement d’applications Microsoft Project Online pour utiliser le CSOM.</span><span class="sxs-lookup"><span data-stu-id="0a09b-104">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="0a09b-105">Nous vous recommandons de découvrir le développement d’applications à l’aide d’un [nouveau projet pour le web](https://developer.microsoft.com/fr-FR/office/blogs/developing-applications-and-reports-using-the-new-project/).</span><span class="sxs-lookup"><span data-stu-id="0a09b-105">We recommend you explore how to develop applications using the [new Project for the web](https://developer.microsoft.com/fr-FR/office/blogs/developing-applications-and-reports-using-the-new-project/).</span></span>
  
## <a name="background"></a><span data-ttu-id="0a09b-106">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="0a09b-106">Background</span></span>

<span data-ttu-id="0a09b-107">L’application Microsoft Project a été créée comme application de bureau au début des années 1990.</span><span class="sxs-lookup"><span data-stu-id="0a09b-107">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="0a09b-108">Aujourd’hui, Project est beaucoup plus que ça, comme en témoignent ses nombreuses versions :</span><span class="sxs-lookup"><span data-stu-id="0a09b-108">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="0a09b-109">Project Standard Edition est une application de bureau qui s’exécute comme une application autonome.</span><span class="sxs-lookup"><span data-stu-id="0a09b-109">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="0a09b-110">Project Professional Edition est une application de bureau capable d’interagir et de partager des données avec un serveur plus important, ainsi que d’exécuter les fonctionnalités disponibles dans Project Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="0a09b-110">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="0a09b-111">Microsoft Project Online est un service hébergé par Microsoft qui fournit aux sociétés une solution de bureau de gestion des projets (PMO) afin de coordonner et de gérer des projets, des programmes et des portefeuilles.</span><span class="sxs-lookup"><span data-stu-id="0a09b-111">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="0a09b-112">Différent des éditions de bureau, Microsoft Project Online peut conserver et effectuer le suivi des détails des projets tout au long de la vie de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="0a09b-112">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="0a09b-113">Project Server est un service hébergé par l’entreprise grâce auquel l’entreprise gère et sécurise le serveur contenant les informations relatives aux projets, aux programmes et aux portefeuilles.</span><span class="sxs-lookup"><span data-stu-id="0a09b-113">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="0a09b-114">Afin de sécuriser le serveur interne, Project Server offre les fonctionnalités orientées projet, programme et portefeuille de l’application Microsoft Project Online hébergée en externe avec une plus grande capacité de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="0a09b-114">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="0a09b-115">Microsoft Project Online dispose de trois ensembles d’API en ligne : modèle objet côté client (CSOM), objet modèle JavaScript (JSOM) et Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="0a09b-115">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="0a09b-116">L’implémentation .NET CSOM est l’interface par défaut lorsque vous développez des applications Windows qui interagissent avec des clients Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="0a09b-116">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="0a09b-117">Les environnements classiques pour les applications centrées sur l’utilisateur incluent les bureaux Windows et les appareils Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="0a09b-117">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="0a09b-118">Les applications principales écrites avec .NET CSOM peuvent se connecter à d’autres serveurs pour la logique métier et les sources de données externes à Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="0a09b-118">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="0a09b-119">Les demandes de récupération sur Microsoft Project Online utilisent un système de requête similaire à LINQ qui propose plusieurs améliorations par rapport aux fonctions de récupération de base.</span><span class="sxs-lookup"><span data-stu-id="0a09b-119">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="0a09b-120">L’interface de modèle objet JavaScript (JSOM) fournit une prise en charge multinavigateur pour les compléments Microsoft Project Online. Un complément est une application web stockée dans le client Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="0a09b-120">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="0a09b-121">Lorsqu’un utilisateur souhaite exécuter un complément, le code du complément se télécharge et s’exécute dans le navigateur de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a09b-121">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="0a09b-122">Le modèle REST/Odata assure la communication basée sur HTTP. Cette interface est recommandée pour les applications dans les environnements non Windows.</span><span class="sxs-lookup"><span data-stu-id="0a09b-122">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="0a09b-123">Les points de terminaison de communication correspondent aux objets du site Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="0a09b-123">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="0a09b-124">Les résultats fournissent des codes d’état HTTP normaux.</span><span class="sxs-lookup"><span data-stu-id="0a09b-124">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="0a09b-125">Cet article traite d’une application qui utilise l’interface .NET CSOM.</span><span class="sxs-lookup"><span data-stu-id="0a09b-125">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="0a09b-126">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="0a09b-126">Prerequisites</span></span>

<span data-ttu-id="0a09b-127">Commencez avec un système de base exécutant Windows 10 et ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a09b-127">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="0a09b-128">.Net Framework 4.0 ou version ultérieure : utilisez la structure complète.</span><span class="sxs-lookup"><span data-stu-id="0a09b-128">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="0a09b-129">Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="0a09b-129">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="0a09b-130">Visual Studio 2013 ou version ultérieure : toutes les éditions sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="0a09b-130">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="0a09b-131">L’édition Community Edition de Visual Studio 2015 a été utilisée pour développer l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="0a09b-131">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="0a09b-132">L’édition Community Edition est disponible à l’adresse suivante https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="0a09b-132">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="0a09b-133">Kit de développement logiciel (SDK) des composants clients de SharePoint : les applications Microsoft Project Online et Project Server sont supérieures à SharePoint et aux assemblys SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0a09b-133">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="0a09b-134">Les composants client de SharePoint sont inclus dans les éditions Visual Studio Professional et Enterprise.</span><span class="sxs-lookup"><span data-stu-id="0a09b-134">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="0a09b-135">Si vous utilisez Visual Studio Community Edition, la dernière version du kit de développement logiciel des outils de développement Office est disponible sur le site suivant : https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="0a09b-135">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="0a09b-136">Compte Microsoft Project Online : permet d’accéder au site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="0a09b-136">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="0a09b-137">Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="0a09b-137">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="0a09b-138">Projets sur le site d’hébergement alimentés avec des informations</span><span class="sxs-lookup"><span data-stu-id="0a09b-138">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="0a09b-139">La structure .NET Framework standard (4.0 ou version ultérieure) est la structure correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0a09b-139">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="0a09b-140">N’utilisez pas le profil client .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="0a09b-140">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="0a09b-141">Développer l’application</span><span class="sxs-lookup"><span data-stu-id="0a09b-141">Develop the application</span></span>

<span data-ttu-id="0a09b-142">Dans le cadre du développement d’une application de bureau pour SharePoint, l’interface par défaut est le modèle objet côté client (CSOM) Project.</span><span class="sxs-lookup"><span data-stu-id="0a09b-142">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="0a09b-143">Vous pouvez télécharger des [exemples de projet CSOM](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) depuis la galerie de ressources du Développeur Project dans le Centre de développement Office.</span><span class="sxs-lookup"><span data-stu-id="0a09b-143">You can download the [Project CSOM samples](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) from the Project Developer resource gallery on the Office Dev Center.</span></span>
  
<span data-ttu-id="0a09b-144">Les deux premières rubriques traitent des questions de base : créer un projet Visual Studio avec des assemblys et des espaces de noms appropriés, et accéder au serveur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="0a09b-144">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="0a09b-145">Les rubriques restantes traitent de la récupération des informations à l’aide du modèle CSOM, à partir d’un ou de plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="0a09b-145">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="0a09b-146">La récupération des informations à partir de l’hôte est un processus en deux actions des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="0a09b-146">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="0a09b-147">Tout d’abord, l’application spécifie et envoie une ou plusieurs demandes de récupération au serveur.</span><span class="sxs-lookup"><span data-stu-id="0a09b-147">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="0a09b-148">Ensuite, l’application transmet une notification au serveur pour exécuter les requêtes soumises.</span><span class="sxs-lookup"><span data-stu-id="0a09b-148">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="0a09b-149">Le serveur répond en envoyant les résultats des requêtes au client.</span><span class="sxs-lookup"><span data-stu-id="0a09b-149">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="0a09b-150">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a09b-150">Set up the Visual Studio project</span></span>

<span data-ttu-id="0a09b-151">La configuration de l’application consiste à créer un nouveau projet, lier les assemblys appropriés et déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0a09b-151">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="0a09b-152">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="0a09b-152">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="0a09b-153">Sélectionner un projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a09b-153">Select a Visual Studio project</span></span>

1. <span data-ttu-id="0a09b-154">Démarrez Visual Studio et sélectionnez **Démarrer un nouveau projet** sur la page de démarrage.</span><span class="sxs-lookup"><span data-stu-id="0a09b-154">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="0a09b-155">La boîte de dialogue Nouveau projet affiche les modèles d’application disponibles et les champs de données pour n’importe quel modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0a09b-155">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="0a09b-156">Pour cette application, spécifiez les éléments indiqués ci-après.</span><span class="sxs-lookup"><span data-stu-id="0a09b-156">For this application, specify the following items.</span></span> <span data-ttu-id="0a09b-157">Les mots-clés rencontrés à l’écran ont un attribut gras :</span><span class="sxs-lookup"><span data-stu-id="0a09b-157">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="0a09b-158">À partir des modèles installés dans le volet gauche, sélectionnez **C#** => **Windows** => **Bureau classique**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-158">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="0a09b-159">En haut du volet central, sélectionnez **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-159">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="0a09b-160">Dans les types d’application situés dans le volet central, sélectionnez **Application console**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-160">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="0a09b-161">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="0a09b-161">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="0a09b-162">Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-162">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="0a09b-163">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="0a09b-163">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="0a09b-164">Ajouter des assemblys</span><span class="sxs-lookup"><span data-stu-id="0a09b-164">Add assemblies</span></span>

<span data-ttu-id="0a09b-165">La solution VS a besoin de l’assembly ProjectServerClient du kit de développement logiciel (SDK) Project 2103, deux assemblys du kit de développement logiciel (SDK) SharePoint et l’assembly .NET Framework System.Security.</span><span class="sxs-lookup"><span data-stu-id="0a09b-165">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="0a09b-166">Dans l’Explorateur de solutions VS, cliquez avec le bouton droit sur l’entrée Références, puis sélectionnez **Ajouter une référence...**</span><span class="sxs-lookup"><span data-stu-id="0a09b-166">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="0a09b-167">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0a09b-167">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="0a09b-168">Sélectionnez **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-168">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="0a09b-169">Le cas échéant, cliquez sur le bouton **Parcourir...**</span><span class="sxs-lookup"><span data-stu-id="0a09b-169">If needed, click the **Browse…**</span></span> <span data-ttu-id="0a09b-170">situé en bas de la boîte de dialogue et accédez au répertoire d’installation du kit de développement logiciel (SDK) Project 2013 pour localiser l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0a09b-170">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="0a09b-171">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-171">Click **OK**.</span></span> 
    
4. <span data-ttu-id="0a09b-172">Ajoutez l’espace de noms ProjectServerClient au fichier .cs.</span><span class="sxs-lookup"><span data-stu-id="0a09b-172">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="0a09b-173">Ajoutez les assemblys du kit de développement logiciel (SDK) SharePoint 2013 à l’aide de la console du Gestionnaire de package NuGet.</span><span class="sxs-lookup"><span data-stu-id="0a09b-173">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="0a09b-174">Dans le menu Outils VS, cliquez sur les menus suivants : **Outils =\> Gestionnaire de package NuGet =\> Console du Gestionnaire de package**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-174">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="0a09b-175">Dans le menu Console du Gestionnaire de package, saisissez la commande suivante, puis appuyez sur \<ENTRÉE\> :</span><span class="sxs-lookup"><span data-stu-id="0a09b-175">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="0a09b-176">La **Console du Gestionnaire de package** fournit une description des résultats de la commande ; et l’Explorateur de solutions VS affiche les assemblys SharePoint dans les références de projet.</span><span class="sxs-lookup"><span data-stu-id="0a09b-176">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="0a09b-177">Ajoutez les espaces de noms dans le fichier .cs :</span><span class="sxs-lookup"><span data-stu-id="0a09b-177">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="0a09b-178">L’assembly System.Security fait partie du .NET Framework et a été installé avec l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="0a09b-178">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="0a09b-179">L’exemple d’application a besoin d’un autre espace de noms qui fournit une chaîne chiffrée au système d’hébergement pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="0a09b-179">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="0a09b-180">Une fois authentifiée, l’application peut accéder aux projets sur le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="0a09b-180">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="0a09b-181">Ajoutez l’espace de noms System.Security au fichier .cs comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a09b-181">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="0a09b-182">Dans l’Explorateur de solutions VS, cliquez avec le bouton droit sur l’entrée Références, puis sélectionnez **Ajouter une référence...**</span><span class="sxs-lookup"><span data-stu-id="0a09b-182">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="0a09b-183">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0a09b-183">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="0a09b-184">Sélectionnez **Assemblys =\> Framework** dans le volet gauche de la boîte de dialogue Gestionnaire de références, puis cliquez sur **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-184">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="0a09b-185">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a09b-185">Click **OK**.</span></span> 
    
4. <span data-ttu-id="0a09b-186">Ajoutez l’espace de noms System.Security au fichier .cs :</span><span class="sxs-lookup"><span data-stu-id="0a09b-186">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="0a09b-187">Le début du fichier .cs doit contenir les espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="0a09b-187">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="0a09b-188">Système</span><span class="sxs-lookup"><span data-stu-id="0a09b-188">System</span></span>
    
- <span data-ttu-id="0a09b-189">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="0a09b-189">System.Collections.Generic</span></span>
    
- <span data-ttu-id="0a09b-190">System.Linq</span><span class="sxs-lookup"><span data-stu-id="0a09b-190">System.Linq</span></span>
    
- <span data-ttu-id="0a09b-191">System.Test</span><span class="sxs-lookup"><span data-stu-id="0a09b-191">System.Test</span></span>
    
- <span data-ttu-id="0a09b-192">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="0a09b-192">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="0a09b-193">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="0a09b-193">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="0a09b-194">System.Security</span><span class="sxs-lookup"><span data-stu-id="0a09b-194">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="0a09b-195">Se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="0a09b-195">Connect to the host system</span></span>

<span data-ttu-id="0a09b-196">Étant donné que Microsoft Project Online est une application SharePoint, utiliser l’authentification SharePoint est l’approche correcte.</span><span class="sxs-lookup"><span data-stu-id="0a09b-196">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="0a09b-197">Le fragment de code suivant prépare l’accès à l’environnement hébergé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-197">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="0a09b-198">Pour préparer l’accès à l’environnement hébergé, effectuez les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a09b-198">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="0a09b-199">Créez un objet de contexte pour les projets : il est inclus dans le code suivant du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="0a09b-199">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="0a09b-200">Le contexte est hérité par d’autres composants autorisant le système à gérer le contexte du modèle objet Project.</span><span class="sxs-lookup"><span data-stu-id="0a09b-200">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="0a09b-201">Identifiez le site hôte : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="0a09b-201">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="0a09b-202">Dans le cadre de l’initialisation du contexte de projets, l’application doit fournir la racine de la collection de sites de projets.</span><span class="sxs-lookup"><span data-stu-id="0a09b-202">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="0a09b-203">L’application utilise une sous-chaîne de l’URL de la racine des projets.</span><span class="sxs-lookup"><span data-stu-id="0a09b-203">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="0a09b-204">Une capture instantanée de cet emplacement est mise en évidence par un rectangle rouge dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0a09b-204">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="0a09b-205">L’authentification a besoin de la chaîne à partir du début jusqu’à la sous-chaîne « pwa ».</span><span class="sxs-lookup"><span data-stu-id="0a09b-205">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="0a09b-206">Dans la liste de code, l’application utilise la chaîne « https://XXXXXXXX.sharepoint.com/sites/pwa ».</span><span class="sxs-lookup"><span data-stu-id="0a09b-206">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="0a09b-207">![Capture d’écran de l’URL de la collection de sites de projets entourée d’une bordure rouge.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Capture d’écran de l’URL de la collection de sites de projets entourée d’une bordure rouge")</span><span class="sxs-lookup"><span data-stu-id="0a09b-207">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border.")</span></span>
  
3. <span data-ttu-id="0a09b-208">Placez le mot de passe dans une chaîne sûre : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="0a09b-208">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="0a09b-209">Le mot de passe et le compte d’utilisateur sont les informations d’identification d’accès au site hôte.</span><span class="sxs-lookup"><span data-stu-id="0a09b-209">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="0a09b-210">Ajoutez le compte d’utilisateur et le mot de passe dans la partie des informations d’identification de l’objet de contexte : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="0a09b-210">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="0a09b-211">Le contexte de projet instancié est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-211">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="0a09b-212">Répertorier tous les projets publiés</span><span class="sxs-lookup"><span data-stu-id="0a09b-212">List all published projects</span></span>

<span data-ttu-id="0a09b-213">Microsoft Project Online et ProjectServer utilisent des proxys pour communiquer avec le serveur afin d’exécuter les opérations créer, signaler, mettre à jour et supprimer (CRUD).</span><span class="sxs-lookup"><span data-stu-id="0a09b-213">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="0a09b-214">L’hôte/le serveur gère les demandes efficacement et permet au client d’effectuer les actions suivantes quand il communique avec le serveur :</span><span class="sxs-lookup"><span data-stu-id="0a09b-214">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="0a09b-215">Établir un contexte pour la communication.</span><span class="sxs-lookup"><span data-stu-id="0a09b-215">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="0a09b-216">Le contexte est utilisé par la collection de projets, ainsi que par d’autres objets et collections via l’héritage, notamment la collection de tâches, la collection d’affectations, l’objet étape et les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0a09b-216">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="0a09b-217">Utilisez le modèle objet pour spécifier un objet, la collection ou les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0a09b-217">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="0a09b-218">Cette étape utilise LINQ comme une requête ou comme une méthode.</span><span class="sxs-lookup"><span data-stu-id="0a09b-218">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="0a09b-219">La spécification contrôle ce que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="0a09b-219">The specification controls what you receive.</span></span> <span data-ttu-id="0a09b-220">Cette étape est souvent incorporée en tant que corps de la méthode de chargement (étape 3).</span><span class="sxs-lookup"><span data-stu-id="0a09b-220">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="0a09b-221">Chargez la spécification de récupération à partir de l’étape précédente en utilisant la méthode Load() ou LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="0a09b-221">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="0a09b-222">Pour charger des collections et des objets, utilisez Load().</span><span class="sxs-lookup"><span data-stu-id="0a09b-222">For loading collections and objects, use Load().</span></span> <span data-ttu-id="0a09b-223">Pour les requêtes avec des clauses telles que « where » et « group », utilisez LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="0a09b-223">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="0a09b-224">Exécutez la demande à l’aide de la méthode ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="0a09b-224">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="0a09b-225">La méthode ExecuteQuery() avertit l’hôte que les requêtes sont prêtes à être exécutées.</span><span class="sxs-lookup"><span data-stu-id="0a09b-225">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="0a09b-226">Une fois que l’hôte a reçu la notification, il exécute les requêtes et envoie les résultats au client.</span><span class="sxs-lookup"><span data-stu-id="0a09b-226">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="0a09b-227">Lorsque le client dispose des informations, l’application peut les utiliser.</span><span class="sxs-lookup"><span data-stu-id="0a09b-227">With the information at the client, the application can use it.</span></span> <span data-ttu-id="0a09b-228">Le fragment de code suivant passe dans les projets publiés et imprime l’ID et le nom de chaque projet publié sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0a09b-228">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="0a09b-229">Résultat :</span><span class="sxs-lookup"><span data-stu-id="0a09b-229">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="0a09b-230">Faire une demande</span><span class="sxs-lookup"><span data-stu-id="0a09b-230">Make a request</span></span>

<span data-ttu-id="0a09b-231">En utilisant les actions du fragment de code précédent, l’application récupère la liste des projets dans le compte spécifié sur le site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="0a09b-231">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="0a09b-232">L’élément ProjectContext est spécifié pour les projets à répertorier.</span><span class="sxs-lookup"><span data-stu-id="0a09b-232">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="0a09b-233">Spécifiez l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0a09b-233">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="0a09b-234">En indiquant uniquement la collection, le serveur récupère la collection de projets, renseignant chaque projet avec les valeurs pour l’ensemble des propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="0a09b-234">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="0a09b-235">Accéder aux propriétés qui font partie de l’ensemble de propriétés par défaut donne des résultats positifs.</span><span class="sxs-lookup"><span data-stu-id="0a09b-235">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="0a09b-236">Accéder à des propriétés qui ne font pas partie de l’ensemble par défaut renvoie une exception « Non initialisé ».</span><span class="sxs-lookup"><span data-stu-id="0a09b-236">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="0a09b-237">Chargez la demande (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="0a09b-237">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="0a09b-238">Cette opération fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0a09b-238">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="0a09b-239">Exécutez la requête (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="0a09b-239">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="0a09b-240">Récupérer des informations de projet de niveau élevé</span><span class="sxs-lookup"><span data-stu-id="0a09b-240">Retrieve high-level project information</span></span>

<span data-ttu-id="0a09b-241">Les propriétés qui ne sont pas des propriétés par défaut doivent être spécifiées dans la demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="0a09b-241">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="0a09b-242">Le fragment de code suivant charge le contexte de collection de projets comme dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0a09b-242">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="0a09b-243">Ensuite, la spécification requiert des propriétés supplémentaires non définies par défaut à inclure dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="0a09b-243">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="0a09b-244">L’instruction de chargement spécifie le contexte de la collection de projets, et ajoute les objets StartDate, Phase et Stage au résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="0a09b-244">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="0a09b-245">Les propriétés supplémentaires peuvent être scalaires, des objets ou des collections.</span><span class="sxs-lookup"><span data-stu-id="0a09b-245">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="0a09b-246">Les éléments scalaires sont directement accessibles.</span><span class="sxs-lookup"><span data-stu-id="0a09b-246">Scalar items can be accessed directly.</span></span> <span data-ttu-id="0a09b-247">Les objets et les collections nécessitent un traitement supplémentaire, comme illustré dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="0a09b-247">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="0a09b-248">Résultat des trois premiers projets :</span><span class="sxs-lookup"><span data-stu-id="0a09b-248">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="0a09b-249">Récupérer toutes les tâches dans un projet</span><span class="sxs-lookup"><span data-stu-id="0a09b-249">Retrieve all tasks in a project</span></span>

<span data-ttu-id="0a09b-250">Chaque projet comporte de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="0a09b-250">Each project has many tasks.</span></span> <span data-ttu-id="0a09b-251">Par conséquent, pour extraire les tâches d’un projet spécifique, effectuez les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a09b-251">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="0a09b-252">Établir le contexte de la collection de projets.</span><span class="sxs-lookup"><span data-stu-id="0a09b-252">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="0a09b-253">Récupérez les informations de projet, y compris les propriétés de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0a09b-253">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="0a09b-254">Notez que l’application traite les projets publiés.</span><span class="sxs-lookup"><span data-stu-id="0a09b-254">Note that the application is addressing published projects.</span></span> <span data-ttu-id="0a09b-255">Le contexte du projet publié actuel est pubProj.</span><span class="sxs-lookup"><span data-stu-id="0a09b-255">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="0a09b-256">Établir le contexte de la collection de tâches.</span><span class="sxs-lookup"><span data-stu-id="0a09b-256">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="0a09b-257">La propriété `pubProj.Tasks` fait référence aux tâches du projet publié actuel.</span><span class="sxs-lookup"><span data-stu-id="0a09b-257">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="0a09b-258">Chargez la spécification pour récupérer la collection de tâches, y compris les propriétés par défaut appropriées.</span><span class="sxs-lookup"><span data-stu-id="0a09b-258">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="0a09b-259">Exécutez la requête pour récupérer la collection de tâches dotées des propriétés appropriées.</span><span class="sxs-lookup"><span data-stu-id="0a09b-259">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="0a09b-260">Les informations sont désormais locales.</span><span class="sxs-lookup"><span data-stu-id="0a09b-260">The information is now local.</span></span> <span data-ttu-id="0a09b-261">Le fragment de code suivant traite la collection de tâches publiées en écrivant les informations sur la console.</span><span class="sxs-lookup"><span data-stu-id="0a09b-261">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="0a09b-262">Résultat des tâches pour un projet :</span><span class="sxs-lookup"><span data-stu-id="0a09b-262">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="0a09b-263">Accéder aux informations à plusieurs niveaux</span><span class="sxs-lookup"><span data-stu-id="0a09b-263">Access information at multiple levels</span></span>

<span data-ttu-id="0a09b-264">Pour chaque tâche, une ou plusieurs personnes (ou</span><span class="sxs-lookup"><span data-stu-id="0a09b-264">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="0a09b-265">ressource) peuvent contribuer à son exécution.</span><span class="sxs-lookup"><span data-stu-id="0a09b-265">resource) contributing toward its completion.</span></span> <span data-ttu-id="0a09b-266">Les collections d’affectations et de ressources contiennent ces informations pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="0a09b-266">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="0a09b-267">Pour assurer le traitement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a09b-267">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="0a09b-268">Obtenez un contexte pour la tâche de projet.</span><span class="sxs-lookup"><span data-stu-id="0a09b-268">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="0a09b-269">Créez une demande et chargez-la pour les affectations liées à la tâche.</span><span class="sxs-lookup"><span data-stu-id="0a09b-269">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="0a09b-270">Exécutez la requête pour les affectations.</span><span class="sxs-lookup"><span data-stu-id="0a09b-270">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="0a09b-271">Créez une demande et chargez-la pour la ressource associée à une affectation individuelle.</span><span class="sxs-lookup"><span data-stu-id="0a09b-271">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="0a09b-272">Exécutez la requête pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="0a09b-272">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="0a09b-273">La collection d’affectations est demandée explicitement dans les informations du serveur, car il ne s’agit pas d’une propriété définie par défaut de la collection de tâches.</span><span class="sxs-lookup"><span data-stu-id="0a09b-273">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="0a09b-274">En tant que collection, une requête ultérieure est faite pour extraire la collection du serveur.</span><span class="sxs-lookup"><span data-stu-id="0a09b-274">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="0a09b-275">La ressource est un objet.</span><span class="sxs-lookup"><span data-stu-id="0a09b-275">The Resource is an object.</span></span> <span data-ttu-id="0a09b-276">La requête associée à une affectation inclut le nom de la ressource associé à l’affectation.</span><span class="sxs-lookup"><span data-stu-id="0a09b-276">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="0a09b-277">Résultat pour les tâches 52, 75 et 76 d’un projet :</span><span class="sxs-lookup"><span data-stu-id="0a09b-277">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="0a09b-278">Accéder aux champs de niveau entreprise personnalisés</span><span class="sxs-lookup"><span data-stu-id="0a09b-278">Access custom enterprise-level fields</span></span>

<span data-ttu-id="0a09b-279">Des champs personnalisés existent pour Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="0a09b-279">Custom fields exist for Project Online.</span></span> <span data-ttu-id="0a09b-280">Il s’agit de champs de niveau entreprise qui peuvent être associés à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="0a09b-280">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="0a09b-281">Cette section explique comment accéder à ces champs.</span><span class="sxs-lookup"><span data-stu-id="0a09b-281">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="0a09b-282">Les champs personnalisés ne sont pas inclus dans l’ensemble de propriétés par défaut associées à un projet.</span><span class="sxs-lookup"><span data-stu-id="0a09b-282">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="0a09b-283">Par conséquent, ils doivent être identifiés explicitement dans le cadre de la spécification de récupération.</span><span class="sxs-lookup"><span data-stu-id="0a09b-283">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="0a09b-284">La vue d’ensemble du processus comprend les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a09b-284">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="0a09b-285">Naviguer jusqu’au champ personnalisé à l’aide de son nom commun.</span><span class="sxs-lookup"><span data-stu-id="0a09b-285">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="0a09b-286">Récupérer le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-286">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="0a09b-287">Revenir au contexte général et interroger le système en utilisant le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-287">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="0a09b-288">Naviguer jusqu’au champ personnalisé, récupérer son nom interne et l’utiliser pour interroger le système</span><span class="sxs-lookup"><span data-stu-id="0a09b-288">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="0a09b-289">Cette tâche spécifie une récupération qui utilise une propriété non définie par défaut avec un détail en plus.</span><span class="sxs-lookup"><span data-stu-id="0a09b-289">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="0a09b-290">Commencez en utilisant le contexte de projets, comme décrit au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="0a09b-290">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="0a09b-291">Ajoutez deux éléments à la demande de récupération de collection de projets en plus de toute autre propriété non définie par défaut à récupérer :</span><span class="sxs-lookup"><span data-stu-id="0a09b-291">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="0a09b-292">La clause `p => p.IncludeCustomFields` identifie la nécessité d’utiliser un objet de projet qui prend en charge les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0a09b-292">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="0a09b-293">La clause `p => p.IncludeCustomFields.CustomFields` requiert l’inclusion des données des champs personnalisés dans le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="0a09b-293">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="0a09b-294">Ces informations sont utilisées une fois que le nom interne du champ personnalisé est récupéré.</span><span class="sxs-lookup"><span data-stu-id="0a09b-294">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="0a09b-295">Rechargez la demande.</span><span class="sxs-lookup"><span data-stu-id="0a09b-295">Load the request.</span></span>
    
   <span data-ttu-id="0a09b-296">Cette opération fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0a09b-296">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="0a09b-297">Exécutez la requête.</span><span class="sxs-lookup"><span data-stu-id="0a09b-297">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="0a09b-298">À l’aide des informations sur le client, créez une demande pour récupérer les champs personnalisés associés au projet actuel.</span><span class="sxs-lookup"><span data-stu-id="0a09b-298">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="0a09b-299">Recherchez le champ personnalisé approprié et récupérez le nom interne du champ.</span><span class="sxs-lookup"><span data-stu-id="0a09b-299">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="0a09b-300">Le nom interne du champ personnalisé est récupéré.</span><span class="sxs-lookup"><span data-stu-id="0a09b-300">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="0a09b-301">Les actions 1 et 2 sont désormais terminées.</span><span class="sxs-lookup"><span data-stu-id="0a09b-301">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="0a09b-302">Revenez au contexte de projet et récupérez la valeur du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-302">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="0a09b-303">La valeur du champ personnalisé est récupérée en utilisant le nom interne comme un index.</span><span class="sxs-lookup"><span data-stu-id="0a09b-303">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="0a09b-304">Résultat de trois projets composés de l’ID du projet, du nom du projet, du nom du champ personnalisé, du nom interne du champ personnalisé et de la valeur du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0a09b-304">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="0a09b-305">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a09b-305">See also</span></span>

<span data-ttu-id="0a09b-306">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/project) dans le Centre de développement Office.</span><span class="sxs-lookup"><span data-stu-id="0a09b-306">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/project).</span></span>
    

