---
title: Développement d’une application Microsoft Project Online à l’aide du modèle objet côté client
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Cet article décrit le développement d’applications Microsoft Project Online pour les applications de bureau à l’aide de .NET Framework 4.0. L’application décrite dans cet article récupère les informations du serveur d’hébergement.
localization_priority: Priority
ms.openlocfilehash: 3d3c2dd5b896c10dab9a0494288f38610cbc99e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322619"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="b6ee7-104">Développement d’une application Microsoft Project Online à l’aide du modèle objet côté client</span><span class="sxs-lookup"><span data-stu-id="b6ee7-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="b6ee7-105">Cet article décrit le développement d’applications Microsoft Project Online pour les applications de bureau à l’aide de .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="b6ee7-106">L’application décrite dans cet article récupère les informations du serveur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="b6ee7-107">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="b6ee7-107">Background</span></span>

<span data-ttu-id="b6ee7-108">L’application Microsoft Project a été créée comme application de bureau au début des années 1990.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="b6ee7-109">Aujourd’hui, Project est beaucoup plus que ça, comme en témoignent ses nombreuses versions :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="b6ee7-110">Project Standard Edition est une application de bureau qui s’exécute comme une application autonome.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="b6ee7-111">Project Professional Edition est une application de bureau capable d’interagir et de partager des données avec un serveur plus important, ainsi que d’exécuter les fonctionnalités disponibles dans Project Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="b6ee7-112">Microsoft Project Online est un service hébergé par Microsoft qui fournit aux sociétés une solution de bureau de gestion des projets (PMO) afin de coordonner et de gérer des projets, des programmes et des portefeuilles.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="b6ee7-113">Différent des éditions de bureau, Microsoft Project Online peut conserver et effectuer le suivi des détails des projets tout au long de la vie de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="b6ee7-114">Project Server est un service hébergé par l’entreprise grâce auquel l’entreprise gère et sécurise le serveur contenant les informations relatives aux projets, aux programmes et aux portefeuilles.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="b6ee7-115">Afin de sécuriser le serveur interne, Project Server offre les fonctionnalités orientées projet, programme et portefeuille de l’application Microsoft Project Online hébergée en externe avec une plus grande capacité de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="b6ee7-116">Microsoft Project Online dispose de trois ensembles d’API en ligne : modèle objet côté client (CSOM), objet modèle JavaScript (JSOM) et Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="b6ee7-117">L’implémentation .NET CSOM est l’interface par défaut lorsque vous développez des applications Windows qui interagissent avec des clients Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="b6ee7-118">Les environnements classiques pour les applications centrées sur l’utilisateur incluent les bureaux Windows et les appareils Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="b6ee7-119">Les applications principales écrites avec .NET CSOM peuvent se connecter à d’autres serveurs pour la logique métier et les sources de données externes à Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="b6ee7-120">Les demandes de récupération sur Microsoft Project Online utilisent un système de requête similaire à LINQ qui propose plusieurs améliorations par rapport aux fonctions de récupération de base.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="b6ee7-121">L’interface de modèle objet JavaScript (JSOM) fournit une prise en charge multinavigateur pour les compléments Microsoft Project Online. Un complément est une application web stockée dans le client Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="b6ee7-122">Lorsqu’un utilisateur souhaite exécuter un complément, le code du complément se télécharge et s’exécute dans le navigateur de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="b6ee7-123">Le modèle REST/Odata assure la communication basée sur HTTP. Cette interface est recommandée pour les applications dans les environnements non Windows.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="b6ee7-124">Les points de terminaison de communication correspondent aux objets du site Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="b6ee7-125">Les résultats fournissent des codes d’état HTTP normaux.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="b6ee7-126">Cet article traite d’une application qui utilise l’interface .NET CSOM.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="b6ee7-127">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b6ee7-127">Prerequisites</span></span>

<span data-ttu-id="b6ee7-128">Commencez avec un système de base exécutant Windows 10 et ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="b6ee7-129">.Net Framework 4.0 ou version ultérieure : utilisez la structure complète.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="b6ee7-130">Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-130">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="b6ee7-131">Visual Studio 2013 ou version ultérieure : toutes les éditions sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="b6ee7-132">L’édition Community Edition de Visual Studio 2015 a été utilisée pour développer l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="b6ee7-133">L’édition Community Edition est disponible à l’adresse suivante https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="b6ee7-134">Kit de développement logiciel (SDK) des composants clients de SharePoint : les applications Microsoft Project Online et Project Server sont supérieures à SharePoint et aux assemblys SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="b6ee7-135">Les composants client de SharePoint sont inclus dans les éditions Visual Studio Professional et Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="b6ee7-136">Si vous utilisez Visual Studio Community Edition, la dernière version du kit de développement logiciel des outils de développement Office est disponible sur le site suivant : https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="b6ee7-137">Compte Microsoft Project Online : permet d’accéder au site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="b6ee7-138">Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="b6ee7-139">Projets sur le site d’hébergement alimentés avec des informations</span><span class="sxs-lookup"><span data-stu-id="b6ee7-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="b6ee7-140">La structure .NET Framework standard (4.0 ou version ultérieure) est la structure correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="b6ee7-141">N’utilisez pas le profil client .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="b6ee7-142">Développer l’application</span><span class="sxs-lookup"><span data-stu-id="b6ee7-142">Develop the application</span></span>

<span data-ttu-id="b6ee7-143">Dans le cadre du développement d’une application de bureau pour SharePoint, l’interface par défaut est le modèle objet côté client (CSOM) Project.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="b6ee7-144">Vous pouvez télécharger l’exemple complet dans https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="b6ee7-145">Les deux premières rubriques traitent des questions de base : créer un projet Visual Studio avec des assemblys et des espaces de noms appropriés, et accéder au serveur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="b6ee7-146">Les rubriques restantes traitent de la récupération des informations à l’aide du modèle CSOM, à partir d’un ou de plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="b6ee7-147">La récupération des informations à partir de l’hôte est un processus en deux actions des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="b6ee7-148">Tout d’abord, l’application spécifie et envoie une ou plusieurs demandes de récupération au serveur.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="b6ee7-149">Ensuite, l’application transmet une notification au serveur pour exécuter les requêtes soumises.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="b6ee7-150">Le serveur répond en envoyant les résultats des requêtes au client.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="b6ee7-151">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6ee7-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="b6ee7-152">La configuration de l’application consiste à créer un nouveau projet, lier les assemblys appropriés et déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="b6ee7-153">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="b6ee7-154">Sélectionner un projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6ee7-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="b6ee7-155">Démarrez Visual Studio et sélectionnez **Démarrer un nouveau projet** sur la page de démarrage.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="b6ee7-156">La boîte de dialogue Nouveau projet affiche les modèles d’application disponibles et les champs de données pour n’importe quel modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="b6ee7-157">Pour cette application, spécifiez les éléments indiqués ci-après.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-157">For this application, specify the following items.</span></span> <span data-ttu-id="b6ee7-158">Les mots-clés rencontrés à l’écran ont un attribut gras :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="b6ee7-159">À partir des modèles installés dans le volet gauche, sélectionnez **C#** => **Windows** => **Bureau classique**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="b6ee7-160">En haut du volet central, sélectionnez **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="b6ee7-161">Dans les types d’application situés dans le volet central, sélectionnez **Application console**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="b6ee7-162">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="b6ee7-163">Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="b6ee7-164">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="b6ee7-165">Ajouter des assemblys</span><span class="sxs-lookup"><span data-stu-id="b6ee7-165">Add assemblies</span></span>

<span data-ttu-id="b6ee7-166">La solution VS a besoin de l’assembly ProjectServerClient du kit de développement logiciel (SDK) Project 2103, deux assemblys du kit de développement logiciel (SDK) SharePoint et l’assembly .NET Framework System.Security.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="b6ee7-167">Dans l’Explorateur de solutions VS, cliquez avec le bouton droit sur l’entrée Références, puis sélectionnez **Ajouter une référence...**</span><span class="sxs-lookup"><span data-stu-id="b6ee7-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="b6ee7-168">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="b6ee7-169">Sélectionnez **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="b6ee7-170">Le cas échéant, cliquez sur le bouton **Parcourir...**</span><span class="sxs-lookup"><span data-stu-id="b6ee7-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="b6ee7-171">situé en bas de la boîte de dialogue et accédez au répertoire d’installation du kit de développement logiciel (SDK) Project 2013 pour localiser l’assembly.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="b6ee7-172">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="b6ee7-173">Ajoutez l’espace de noms ProjectServerClient au fichier .cs.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="b6ee7-174">Ajoutez les assemblys du kit de développement logiciel (SDK) SharePoint 2013 à l’aide de la console du Gestionnaire de package NuGet.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="b6ee7-175">Dans le menu Outils VS, cliquez sur les menus suivants : **Outils =\> Gestionnaire de package NuGet =\> Console du Gestionnaire de package**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="b6ee7-176">Dans le menu Console du Gestionnaire de package, saisissez la commande suivante, puis appuyez sur \<ENTRÉE\> :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="b6ee7-177">La **Console du Gestionnaire de package** fournit une description des résultats de la commande ; et l’Explorateur de solutions VS affiche les assemblys SharePoint dans les références de projet.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="b6ee7-178">Ajoutez les espaces de noms dans le fichier .cs :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="b6ee7-179">L’assembly System.Security fait partie du .NET Framework et a été installé avec l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="b6ee7-180">L’exemple d’application a besoin d’un autre espace de noms qui fournit une chaîne chiffrée au système d’hébergement pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="b6ee7-181">Une fois authentifiée, l’application peut accéder aux projets sur le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="b6ee7-182">Ajoutez l’espace de noms System.Security au fichier .cs comme suit :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="b6ee7-183">Dans l’Explorateur de solutions VS, cliquez avec le bouton droit sur l’entrée Références, puis sélectionnez **Ajouter une référence...**</span><span class="sxs-lookup"><span data-stu-id="b6ee7-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="b6ee7-184">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="b6ee7-185">Sélectionnez **Assemblys =\> Framework** dans le volet gauche de la boîte de dialogue Gestionnaire de références, puis cliquez sur **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="b6ee7-186">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="b6ee7-187">Ajoutez l’espace de noms System.Security au fichier .cs :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="b6ee7-188">Le début du fichier .cs doit contenir les espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="b6ee7-189">Système</span><span class="sxs-lookup"><span data-stu-id="b6ee7-189">System</span></span>
    
- <span data-ttu-id="b6ee7-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="b6ee7-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="b6ee7-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="b6ee7-191">System.Linq</span></span>
    
- <span data-ttu-id="b6ee7-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="b6ee7-192">System.Test</span></span>
    
- <span data-ttu-id="b6ee7-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="b6ee7-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="b6ee7-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="b6ee7-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="b6ee7-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="b6ee7-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="b6ee7-196">Se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="b6ee7-196">Connect to the host system</span></span>

<span data-ttu-id="b6ee7-197">Étant donné que Microsoft Project Online est une application SharePoint, utiliser l’authentification SharePoint est l’approche correcte.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="b6ee7-198">Le fragment de code suivant prépare l’accès à l’environnement hébergé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-198">The following code fragment prepares to access the hosted environment.</span></span>
  
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

<span data-ttu-id="b6ee7-199">Pour préparer l’accès à l’environnement hébergé, effectuez les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="b6ee7-200">Créez un objet de contexte pour les projets : il est inclus dans le code suivant du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="b6ee7-201">Le contexte est hérité par d’autres composants autorisant le système à gérer le contexte du modèle objet Project.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="b6ee7-202">Identifiez le site hôte : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="b6ee7-203">Dans le cadre de l’initialisation du contexte de projets, l’application doit fournir la racine de la collection de sites de projets.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="b6ee7-204">L’application utilise une sous-chaîne de l’URL de la racine des projets.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="b6ee7-205">Une capture instantanée de cet emplacement est mise en évidence par un rectangle rouge dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="b6ee7-206">L’authentification a besoin de la chaîne à partir du début jusqu’à la sous-chaîne « pwa ».</span><span class="sxs-lookup"><span data-stu-id="b6ee7-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="b6ee7-207">Dans la liste de code, l’application utilise la chaîne « https://XXXXXXXX.sharepoint.com/sites/pwa ».</span><span class="sxs-lookup"><span data-stu-id="b6ee7-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="b6ee7-208">![Capture d’écran de l’URL de la collection de sites de projets entourée d’une bordure rouge.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Capture d’écran de l’URL de la collection de sites de projets entourée d’une bordure rouge")</span><span class="sxs-lookup"><span data-stu-id="b6ee7-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="b6ee7-209">Placez le mot de passe dans une chaîne sûre : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="b6ee7-210">Le mot de passe et le compte d’utilisateur sont les informations d’identification d’accès au site hôte.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="b6ee7-211">Ajoutez le compte d’utilisateur et le mot de passe dans la partie des informations d’identification de l’objet de contexte : cette opération est effectuée dans le code suivant à partir du fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="b6ee7-212">Le contexte de projet instancié est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="b6ee7-213">Répertorier tous les projets publiés</span><span class="sxs-lookup"><span data-stu-id="b6ee7-213">List all published projects</span></span>

<span data-ttu-id="b6ee7-214">Microsoft Project Online et ProjectServer utilisent des proxys pour communiquer avec le serveur afin d’exécuter les opérations créer, signaler, mettre à jour et supprimer (CRUD).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="b6ee7-215">L’hôte/le serveur gère les demandes efficacement et permet au client d’effectuer les actions suivantes quand il communique avec le serveur :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="b6ee7-216">Établir un contexte pour la communication.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="b6ee7-217">Le contexte est utilisé par la collection de projets, ainsi que par d’autres objets et collections via l’héritage, notamment la collection de tâches, la collection d’affectations, l’objet étape et les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="b6ee7-218">Utilisez le modèle objet pour spécifier un objet, la collection ou les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="b6ee7-219">Cette étape utilise LINQ comme une requête ou comme une méthode.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="b6ee7-220">La spécification contrôle ce que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-220">The specification controls what you receive.</span></span> <span data-ttu-id="b6ee7-221">Cette étape est souvent incorporée en tant que corps de la méthode de chargement (étape 3).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="b6ee7-222">Chargez la spécification de récupération à partir de l’étape précédente en utilisant la méthode Load() ou LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="b6ee7-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="b6ee7-223">Pour charger des collections et des objets, utilisez Load().</span><span class="sxs-lookup"><span data-stu-id="b6ee7-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="b6ee7-224">Pour les requêtes avec des clauses telles que « where » et « group », utilisez LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="b6ee7-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="b6ee7-225">Exécutez la demande à l’aide de la méthode ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="b6ee7-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="b6ee7-226">La méthode ExecuteQuery() avertit l’hôte que les requêtes sont prêtes à être exécutées.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="b6ee7-227">Une fois que l’hôte a reçu la notification, il exécute les requêtes et envoie les résultats au client.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="b6ee7-228">Lorsque le client dispose des informations, l’application peut les utiliser.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="b6ee7-229">Le fragment de code suivant passe dans les projets publiés et imprime l’ID et le nom de chaque projet publié sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
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

<span data-ttu-id="b6ee7-230">Résultat :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="b6ee7-231">Faire une demande</span><span class="sxs-lookup"><span data-stu-id="b6ee7-231">Make a request</span></span>

<span data-ttu-id="b6ee7-232">En utilisant les actions du fragment de code précédent, l’application récupère la liste des projets dans le compte spécifié sur le site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="b6ee7-233">L’élément ProjectContext est spécifié pour les projets à répertorier.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="b6ee7-234">Spécifiez l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="b6ee7-235">En indiquant uniquement la collection, le serveur récupère la collection de projets, renseignant chaque projet avec les valeurs pour l’ensemble des propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="b6ee7-236">Accéder aux propriétés qui font partie de l’ensemble de propriétés par défaut donne des résultats positifs.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="b6ee7-237">Accéder à des propriétés qui ne font pas partie de l’ensemble par défaut renvoie une exception « Non initialisé ».</span><span class="sxs-lookup"><span data-stu-id="b6ee7-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="b6ee7-238">Chargez la demande (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="b6ee7-239">Cette opération fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="b6ee7-240">Exécutez la requête (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="b6ee7-241">Récupérer des informations de projet de niveau élevé</span><span class="sxs-lookup"><span data-stu-id="b6ee7-241">Retrieve high-level project information</span></span>

<span data-ttu-id="b6ee7-242">Les propriétés qui ne sont pas des propriétés par défaut doivent être spécifiées dans la demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="b6ee7-243">Le fragment de code suivant charge le contexte de collection de projets comme dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="b6ee7-244">Ensuite, la spécification requiert des propriétés supplémentaires non définies par défaut à inclure dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="b6ee7-245">L’instruction de chargement spécifie le contexte de la collection de projets, et ajoute les objets StartDate, Phase et Stage au résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="b6ee7-246">Les propriétés supplémentaires peuvent être scalaires, des objets ou des collections.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="b6ee7-247">Les éléments scalaires sont directement accessibles.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="b6ee7-248">Les objets et les collections nécessitent un traitement supplémentaire, comme illustré dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
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

<span data-ttu-id="b6ee7-249">Résultat des trois premiers projets :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-249">Output of the first three projects:</span></span>
  
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

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="b6ee7-250">Récupérer toutes les tâches dans un projet</span><span class="sxs-lookup"><span data-stu-id="b6ee7-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="b6ee7-251">Chaque projet comporte de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-251">Each project has many tasks.</span></span> <span data-ttu-id="b6ee7-252">Par conséquent, pour extraire les tâches d’un projet spécifique, effectuez les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="b6ee7-253">Établir le contexte de la collection de projets.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="b6ee7-254">Récupérez les informations de projet, y compris les propriétés de la tâche.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="b6ee7-255">Notez que l’application traite les projets publiés.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="b6ee7-256">Le contexte du projet publié actuel est pubProj.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="b6ee7-257">Établir le contexte de la collection de tâches.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="b6ee7-258">La propriété `pubProj.Tasks` fait référence aux tâches du projet publié actuel.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="b6ee7-259">Chargez la spécification pour récupérer la collection de tâches, y compris les propriétés par défaut appropriées.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="b6ee7-260">Exécutez la requête pour récupérer la collection de tâches dotées des propriétés appropriées.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="b6ee7-261">Les informations sont désormais locales.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-261">The information is now local.</span></span> <span data-ttu-id="b6ee7-262">Le fragment de code suivant traite la collection de tâches publiées en écrivant les informations sur la console.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
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

<span data-ttu-id="b6ee7-263">Résultat des tâches pour un projet :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-263">Output of tasks for one project:</span></span>
  
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

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="b6ee7-264">Accéder aux informations à plusieurs niveaux</span><span class="sxs-lookup"><span data-stu-id="b6ee7-264">Access information at multiple levels</span></span>

<span data-ttu-id="b6ee7-265">Pour chaque tâche, une ou plusieurs personnes (ou</span><span class="sxs-lookup"><span data-stu-id="b6ee7-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="b6ee7-266">ressource) peuvent contribuer à son exécution.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="b6ee7-267">Les collections d’affectations et de ressources contiennent ces informations pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="b6ee7-268">Pour assurer le traitement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="b6ee7-269">Obtenez un contexte pour la tâche de projet.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="b6ee7-270">Créez une demande et chargez-la pour les affectations liées à la tâche.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="b6ee7-271">Exécutez la requête pour les affectations.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="b6ee7-272">Créez une demande et chargez-la pour la ressource associée à une affectation individuelle.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="b6ee7-273">Exécutez la requête pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="b6ee7-274">La collection d’affectations est demandée explicitement dans les informations du serveur, car il ne s’agit pas d’une propriété définie par défaut de la collection de tâches.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="b6ee7-275">En tant que collection, une requête ultérieure est faite pour extraire la collection du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="b6ee7-276">La ressource est un objet.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-276">The Resource is an object.</span></span> <span data-ttu-id="b6ee7-277">La requête associée à une affectation inclut le nom de la ressource associé à l’affectation.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
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

<span data-ttu-id="b6ee7-278">Résultat pour les tâches 52, 75 et 76 d’un projet :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
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

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="b6ee7-279">Accéder aux champs de niveau entreprise personnalisés</span><span class="sxs-lookup"><span data-stu-id="b6ee7-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="b6ee7-280">Des champs personnalisés existent pour Microsoft Project Online.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="b6ee7-281">Il s’agit de champs de niveau entreprise qui peuvent être associés à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="b6ee7-282">Cette section explique comment accéder à ces champs.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="b6ee7-283">Les champs personnalisés ne sont pas inclus dans l’ensemble de propriétés par défaut associées à un projet.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="b6ee7-284">Par conséquent, ils doivent être identifiés explicitement dans le cadre de la spécification de récupération.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="b6ee7-285">La vue d’ensemble du processus comprend les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="b6ee7-286">Naviguer jusqu’au champ personnalisé à l’aide de son nom commun.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="b6ee7-287">Récupérer le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="b6ee7-288">Revenir au contexte général et interroger le système en utilisant le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="b6ee7-289">Naviguer jusqu’au champ personnalisé, récupérer son nom interne et l’utiliser pour interroger le système</span><span class="sxs-lookup"><span data-stu-id="b6ee7-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="b6ee7-290">Cette tâche spécifie une récupération qui utilise une propriété non définie par défaut avec un détail en plus.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="b6ee7-291">Commencez en utilisant le contexte de projets, comme décrit au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="b6ee7-292">Ajoutez deux éléments à la demande de récupération de collection de projets en plus de toute autre propriété non définie par défaut à récupérer :</span><span class="sxs-lookup"><span data-stu-id="b6ee7-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="b6ee7-293">La clause `p => p.IncludeCustomFields` identifie la nécessité d’utiliser un objet de projet qui prend en charge les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="b6ee7-294">La clause `p => p.IncludeCustomFields.CustomFields` requiert l’inclusion des données des champs personnalisés dans le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="b6ee7-295">Ces informations sont utilisées une fois que le nom interne du champ personnalisé est récupéré.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="b6ee7-296">Rechargez la demande.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-296">Load the request.</span></span>
    
   <span data-ttu-id="b6ee7-297">Cette opération fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="b6ee7-298">Exécutez la requête.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="b6ee7-299">À l’aide des informations sur le client, créez une demande pour récupérer les champs personnalisés associés au projet actuel.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="b6ee7-300">Recherchez le champ personnalisé approprié et récupérez le nom interne du champ.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="b6ee7-301">Le nom interne du champ personnalisé est récupéré.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="b6ee7-302">Les actions 1 et 2 sont désormais terminées.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="b6ee7-303">Revenez au contexte de projet et récupérez la valeur du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="b6ee7-304">La valeur du champ personnalisé est récupérée en utilisant le nom interne comme un index.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="b6ee7-305">Résultat de trois projets composés de l’ID du projet, du nom du projet, du nom du champ personnalisé, du nom interne du champ personnalisé et de la valeur du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b6ee7-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b6ee7-306">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6ee7-306">See also</span></span>

<span data-ttu-id="b6ee7-307">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/fr-FR/project).</span><span class="sxs-lookup"><span data-stu-id="b6ee7-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/fr-FR/project).</span></span>
    

