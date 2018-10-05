---
title: Développement d’une application Project Online à l’aide du modèle objet côté client
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Cet article décrit le développement d’applications Microsoft Project Online pour les applications bureautiques à l’aide de .NET Framework 4.0. L’application décrite dans cet article récupère des informations à partir du serveur d’hébergement.
ms.openlocfilehash: b6e7260fd2337d2b156f97605fdd201f5e0d4edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385262"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="7a165-104">Développement d’une application Project Online à l’aide du modèle objet côté client</span><span class="sxs-lookup"><span data-stu-id="7a165-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="7a165-105">Cet article décrit le développement d’applications Microsoft Project Online pour les applications bureautiques à l’aide de .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="7a165-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="7a165-106">L’application décrite dans cet article récupère des informations à partir du serveur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="7a165-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="7a165-107">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="7a165-107">Background</span></span>

<span data-ttu-id="7a165-108">Microsoft Project en route en tant qu’application de bureau de début des années 90.</span><span class="sxs-lookup"><span data-stu-id="7a165-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="7a165-109">Aujourd'hui, Project est beaucoup plus, comme l’atteste son plusieurs variétés :</span><span class="sxs-lookup"><span data-stu-id="7a165-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="7a165-110">Project standard edition est une application de bureau qui s’exécute en tant qu’application autonome.</span><span class="sxs-lookup"><span data-stu-id="7a165-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="7a165-111">Project professionnelle édition est une application de bureau qui permettre interagir et partager des données avec un serveur à grande échelle, ainsi effectuer les fonctionnalités de Project Édition standard.</span><span class="sxs-lookup"><span data-stu-id="7a165-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="7a165-112">Project Online est un service hébergé par Microsoft qui permet aux entreprises avec une solution de niveau PMO pour coordonner et gérer des portefeuilles, programmes et projets.</span><span class="sxs-lookup"><span data-stu-id="7a165-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="7a165-113">Une offre différente versions du bureau, Project Online permettre gérer et suivre les détails du projet dans toute la durée de vie d’un projet.</span><span class="sxs-lookup"><span data-stu-id="7a165-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="7a165-114">Project Server est un service hébergé de contenu d’entreprise dans lequel l’entreprise gère et sécurise le serveur contenant le projet, programme et informations de portefeuille.</span><span class="sxs-lookup"><span data-stu-id="7a165-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="7a165-115">Project Server, en raison de la sécurisation du serveur interne, offre le projet, programme et les fonctionnalités de portefeuille orienté de hébergé en externe Project Online avec une capacité supérieure pour la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="7a165-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="7a165-116">Project Online comprend trois ensembles d’API en ligne : modèle d’objet côté Client (CSOM) et modèle d’objet JavaScript (JSOM) Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="7a165-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="7a165-117">L’implémentation du modèle CSOM .NET est l’interface par défaut lors du développement d’applications Windows qui interagissent avec les clients Project Online.</span><span class="sxs-lookup"><span data-stu-id="7a165-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="7a165-118">Environnements standard pour les applications orientées utilisateur incluent des ordinateurs de bureau Windows et les appareils Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="7a165-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="7a165-119">Applications principale écrites avec CSOM .NET peuvent se connecter aux autres serveurs de l’entreprise logique et sources de données externes à Project Online.</span><span class="sxs-lookup"><span data-stu-id="7a165-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="7a165-120">Les demandes de récupération pour Project Online utilisent un système de requête LINQ comparables à celles qui offre plusieurs améliorations par rapport à des fonctions de récupération de base.</span><span class="sxs-lookup"><span data-stu-id="7a165-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="7a165-121">L’interface de modèle d’objet JavaScript (JSOM) prend en charge élargie des navigateurs compléments Project Online. Un complément est une application web qui est stockée dans le client Project Online.</span><span class="sxs-lookup"><span data-stu-id="7a165-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="7a165-122">Lorsqu’un utilisateur souhaite exécuter une macro complémentaire, le code de la macro complémentaire télécharge et s’exécute dans le navigateur sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a165-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="7a165-123">Le modèle REST/Odata fournit la communication basé sur HTTP, cette interface est recommandée pour les applications dans des environnements non Windows.</span><span class="sxs-lookup"><span data-stu-id="7a165-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="7a165-124">Points de terminaison de communication sont les objets dans le site Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="7a165-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="7a165-125">Résultats fournissent des codes d’état HTTP normales.</span><span class="sxs-lookup"><span data-stu-id="7a165-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="7a165-126">Cet article se concentre sur une application qui utilise l’interface CSOM .NET.</span><span class="sxs-lookup"><span data-stu-id="7a165-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="7a165-127">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="7a165-127">Prerequisites</span></span>

<span data-ttu-id="7a165-128">Démarrer avec un système de base Windows 10 en cours d’exécution, puis ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="7a165-129">.NET framework 4.0 ou version ultérieure--utilisent l’infrastructure complète.</span><span class="sxs-lookup"><span data-stu-id="7a165-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="7a165-130">Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="7a165-130">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="7a165-131">Visual Studio 2013 ou version ultérieure, n’importe quelle édition est acceptable.</span><span class="sxs-lookup"><span data-stu-id="7a165-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="7a165-132">L’édition de la Communauté de Visual Studio 2015 a été utilisée pour développer l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="7a165-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="7a165-133">L’édition de la Communauté est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="7a165-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="7a165-134">Les composants SharePoint Client SDK--Project Online et Project Server trouvent sur SharePoint et SharePoint assemblys.</span><span class="sxs-lookup"><span data-stu-id="7a165-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="7a165-135">Les composants Client SharePoint sont inclus dans les éditions de Visual Studio Professional et d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7a165-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="7a165-136">Si vous utilisez Visual Studio Community edition, la dernière version du SDK des outils pour développeurs Office est disponible sur le site suivant : https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="7a165-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="7a165-137">Un compte Project Online : cela offre un accès au site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="7a165-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="7a165-138">Pour plus d’informations sur l’obtention d’un compte Project Online, voir https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="7a165-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="7a165-139">Projets sont remplies avec les informations sur le site d’hébergement</span><span class="sxs-lookup"><span data-stu-id="7a165-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="7a165-140">La norme .NET Framework (4.0 ou version ultérieure) est l’infrastructure correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7a165-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="7a165-141">N’utilisez pas le .NET Framework 4 Client Profile.</span><span class="sxs-lookup"><span data-stu-id="7a165-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="7a165-142">Développer l’application</span><span class="sxs-lookup"><span data-stu-id="7a165-142">Develop the application</span></span>

<span data-ttu-id="7a165-143">Dans le développement d’une application de bureau pour SharePoint, l’interface par défaut est le modèle d’objet projet client (CSOM).</span><span class="sxs-lookup"><span data-stu-id="7a165-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="7a165-144">Vous pouvez télécharger l’exemple complet à https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="7a165-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="7a165-145">Les deux premières rubriques traitent des problèmes de base : création d’un projet Visual Studio avec les espaces de noms appropriés et des assemblys et l’accès au serveur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="7a165-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="7a165-146">Les autres rubriques traitent avec la récupération des informations à l’aide du modèle CSOM, à partir d’un et plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="7a165-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="7a165-147">Récupérer des informations sur l’hôte est un processus double action à partir d’applications clientes.</span><span class="sxs-lookup"><span data-stu-id="7a165-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="7a165-148">Tout d’abord, l’application spécifie et envoie une ou plusieurs demandes de récupération pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="7a165-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="7a165-149">Deuxièmement, l’application envoie une notification au serveur pour exécuter les requêtes soumis.</span><span class="sxs-lookup"><span data-stu-id="7a165-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="7a165-150">Le serveur répond en envoyant les résultats de requête au client.</span><span class="sxs-lookup"><span data-stu-id="7a165-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="7a165-151">Configurer le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7a165-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="7a165-152">Configuration de l’application se compose de création d’un nouveau projet, lier les assemblys appropriés et déclarer les espaces de noms nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7a165-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="7a165-153">Visual Studio présente plusieurs types de projets de développement.</span><span class="sxs-lookup"><span data-stu-id="7a165-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="7a165-154">Sélectionnez le projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7a165-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="7a165-155">Démarrez Visual Studio et sélectionnez **Démarrer un nouveau projet** dans la Page de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7a165-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="7a165-156">La boîte de dialogue Nouveau projet affiche les modèles d’application disponibles et les champs de données pour n’importe quel modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7a165-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="7a165-157">Pour cette application, spécifiez les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="7a165-157">For this application, specify the following items.</span></span> <span data-ttu-id="7a165-158">Mots clés rencontrés dans l’écran ont un attribut gras :</span><span class="sxs-lookup"><span data-stu-id="7a165-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="7a165-159">À partir des modèles installés dans le volet gauche, sélectionnez **c#** => **Windows** => **Bureau classique**.</span><span class="sxs-lookup"><span data-stu-id="7a165-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="7a165-160">En haut du volet central, sélectionnez **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="7a165-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="7a165-161">Dans les types d’application dans le volet central, sélectionnez **Application Console**.</span><span class="sxs-lookup"><span data-stu-id="7a165-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="7a165-162">Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.</span><span class="sxs-lookup"><span data-stu-id="7a165-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="7a165-163">Également dans la section inférieure, cochez la case de **créer le répertoire pour la solution** .</span><span class="sxs-lookup"><span data-stu-id="7a165-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="7a165-164">Cliquez sur **OK** pour créer le projet initial.</span><span class="sxs-lookup"><span data-stu-id="7a165-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="7a165-165">Ajouter des assemblys</span><span class="sxs-lookup"><span data-stu-id="7a165-165">Add assemblies</span></span>

<span data-ttu-id="7a165-166">La solution VS doit le 2103 Project SDK, deux assemblys dans le SDK SharePoint et l’assembly .NET Framework System.Security de l’assembly ProjectServerClient.</span><span class="sxs-lookup"><span data-stu-id="7a165-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="7a165-167">Dans l’Explorateur de solutions VS, avec le bouton droit de la saisie de références et sélectionnez **Ajouter une référence**</span><span class="sxs-lookup"><span data-stu-id="7a165-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="7a165-168">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7a165-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="7a165-169">Vérifier la **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="7a165-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="7a165-170">Si nécessaire, cliquez sur **Parcourir...**</span><span class="sxs-lookup"><span data-stu-id="7a165-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="7a165-171">en bas de la boîte de dialogue et accédez au répertoire d’installation du SDK de Project 2013 pour rechercher l’assembly.</span><span class="sxs-lookup"><span data-stu-id="7a165-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="7a165-172">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a165-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="7a165-173">Dans le fichier .cs, ajoutez l’espace de noms PrjoctServer Client.</span><span class="sxs-lookup"><span data-stu-id="7a165-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="7a165-174">Ajoutez les assemblys du Kit de développement SharePoint 2013 à l’aide de la Console du Gestionnaire de Package NuGet.</span><span class="sxs-lookup"><span data-stu-id="7a165-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="7a165-175">Dans le menu Outils VS, cliquez sur les menus suivants : **outils =\> Gestionnaire de Package NuGet =\> Console du Gestionnaire de Package**.</span><span class="sxs-lookup"><span data-stu-id="7a165-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="7a165-176">Dans la Console du Gestionnaire de Package, saisissez les commandes et appuyez sur suivants \<entrée\>:</span><span class="sxs-lookup"><span data-stu-id="7a165-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="7a165-177">La **Console du Gestionnaire de Package** fournit une description des résultats de la commande ; et les assemblys SharePoint pour afficher l’Explorateur de solutions VS dans les références de projet.</span><span class="sxs-lookup"><span data-stu-id="7a165-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="7a165-178">Ajoutez les espaces de noms au fichier .cs :</span><span class="sxs-lookup"><span data-stu-id="7a165-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="7a165-179">L’assembly System.Security fait partie de .NET Framework et a été installé avec l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="7a165-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="7a165-180">L’exemple d’application a besoin d’un espace de noms plus qui fournit une chaîne chiffrée pour le système d’hébergement pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="7a165-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="7a165-181">Une fois authentifiée, l’application peut accéder aux projets sur le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="7a165-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="7a165-182">Ajoutez l’espace de noms System.Security au fichier .cs de cette façon :</span><span class="sxs-lookup"><span data-stu-id="7a165-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="7a165-183">Dans l’Explorateur de solutions VS, avec le bouton droit de la saisie de références et sélectionnez **Ajouter une référence**</span><span class="sxs-lookup"><span data-stu-id="7a165-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="7a165-184">dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7a165-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="7a165-185">Sélectionnez **assemblys =\> Framework** dans le volet gauche de la boîte de dialogue Gestionnaire de références, puis vérifiez **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="7a165-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="7a165-186">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a165-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="7a165-187">Dans le fichier .cs, ajoutez l’espace de noms System.Security :</span><span class="sxs-lookup"><span data-stu-id="7a165-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="7a165-188">Le début du fichier .cs doit contenir des espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="7a165-189">Système</span><span class="sxs-lookup"><span data-stu-id="7a165-189">System</span></span>
    
- <span data-ttu-id="7a165-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="7a165-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="7a165-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="7a165-191">System.Linq</span></span>
    
- <span data-ttu-id="7a165-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="7a165-192">System.Test</span></span>
    
- <span data-ttu-id="7a165-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="7a165-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="7a165-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="7a165-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="7a165-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="7a165-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="7a165-196">Se connecter au système hôte</span><span class="sxs-lookup"><span data-stu-id="7a165-196">Connect to the host system</span></span>

<span data-ttu-id="7a165-197">Project Online est une application SharePoint, à l’aide de l’authentification SharePoint est l’approche correcte.</span><span class="sxs-lookup"><span data-stu-id="7a165-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="7a165-198">Le fragment de code suivant prépare accéder à l’environnement hébergé.</span><span class="sxs-lookup"><span data-stu-id="7a165-198">The following code fragment prepares to access the hosted environment.</span></span>
  
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

<span data-ttu-id="7a165-199">Préparations pour accéder à l’environnement hébergé incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="7a165-200">Créer un objet de contexte pour les projets : est contenu dans le code suivant de l’extrait de code précédent.</span><span class="sxs-lookup"><span data-stu-id="7a165-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="7a165-201">Le contexte est hérité par d’autres composants, autoriser le système à gérer le contexte du modèle objet Project.</span><span class="sxs-lookup"><span data-stu-id="7a165-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="7a165-202">Identifiez le site hôte : cette opération est effectuée dans le code suivant dans le fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="7a165-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="7a165-203">Lors de l’instanciation le contexte de projets, l’application doit fournir la racine de la collection de sites de projets.</span><span class="sxs-lookup"><span data-stu-id="7a165-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="7a165-204">L’application utilise une sous-chaîne de l’URL de la racine des projets.</span><span class="sxs-lookup"><span data-stu-id="7a165-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="7a165-205">Une capture instantanée de cet emplacement est mise en surbrillance avec un rectangle rouge dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7a165-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="7a165-206">L’authentification doit la chaîne à partir de son démarrage par le biais de la sous-chaîne « pwa ».</span><span class="sxs-lookup"><span data-stu-id="7a165-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="7a165-207">Dans le code, l’application utilise la chaîne «https://XXXXXXXX.sharepoint.com/sites/pwa».</span><span class="sxs-lookup"><span data-stu-id="7a165-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="7a165-208">![Capture d’écran de l’URL de la collection de sites de projets au sein d’une bordure rouge.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Capture d’écran de l’URL des projets de site collection au sein d’une bordure rouge")</span><span class="sxs-lookup"><span data-stu-id="7a165-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="7a165-209">Placer le mot de passe dans une chaîne sécurisée : cette opération est effectuée dans le code suivant dans le fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="7a165-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="7a165-210">Le compte d’utilisateur et mot de passe sont les informations d’identification pour accéder au site hôte.</span><span class="sxs-lookup"><span data-stu-id="7a165-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="7a165-211">Ajouter le compte d’utilisateur et le mot de passe à la partie d’informations d’identification de l’objet context : cette opération est effectuée dans le code suivant dans le fragment de code précédent.</span><span class="sxs-lookup"><span data-stu-id="7a165-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="7a165-212">Le contexte du projet instancié est prêt à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7a165-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="7a165-213">Liste des projets publiés tous les</span><span class="sxs-lookup"><span data-stu-id="7a165-213">List all published projects</span></span>

<span data-ttu-id="7a165-214">Project Online ProjectServer proxys permet de communiquer avec le serveur pour créer, rapport, mise à jour et suppression (CRUD).</span><span class="sxs-lookup"><span data-stu-id="7a165-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="7a165-215">Le serveur hôte/traite les demandes de manière efficace et comprend le client à effectuer les actions suivantes pour la communication avec le serveur :</span><span class="sxs-lookup"><span data-stu-id="7a165-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="7a165-216">Établir un contexte pour la communication.</span><span class="sxs-lookup"><span data-stu-id="7a165-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="7a165-217">Le contexte est utilisé par la collection de projets, ainsi que d’autres objets et collections par le biais de l’héritage des autorisations, y compris la collection tasks, collection assignments, l’objet stage et champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7a165-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="7a165-218">Utilisez le modèle objet pour spécifier un objet, collection ou aucune donnée à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7a165-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="7a165-219">Cette étape utilise LINQ sous la forme d’une requête ou une méthode.</span><span class="sxs-lookup"><span data-stu-id="7a165-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="7a165-220">La spécification du contrôle que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="7a165-220">The specification controls what you receive.</span></span> <span data-ttu-id="7a165-221">Souvent, cette étape est incorporée dans le corps de la méthode Load (étape 3).</span><span class="sxs-lookup"><span data-stu-id="7a165-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="7a165-222">Charger la spécification de récupération à partir de l’étape précédente à l’aide de la méthode Load() ou LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="7a165-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="7a165-223">Pour charger des objets et collections, utilisez Load().</span><span class="sxs-lookup"><span data-stu-id="7a165-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="7a165-224">Pour les requêtes comportant des clauses comme « où » et « groupe », utilisez LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="7a165-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="7a165-225">Exécute la demande à l’aide de la méthode ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="7a165-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="7a165-226">La méthode ExecuteQuery() avertit l’hôte que l’ou les requêtes sont prêts à être exécutés.</span><span class="sxs-lookup"><span data-stu-id="7a165-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="7a165-227">Une fois que l’hôte reçoit une notification, il exécute les requêtes et envoie les résultats au client.</span><span class="sxs-lookup"><span data-stu-id="7a165-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="7a165-228">Avec les informations sur le client, l’application peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="7a165-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="7a165-229">Le fragment de code suivant parcourt les projets publiés et imprime l’Id et le nom de chaque projet publié sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7a165-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
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

<span data-ttu-id="7a165-230">Sortie :</span><span class="sxs-lookup"><span data-stu-id="7a165-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="7a165-231">Effectuer une demande</span><span class="sxs-lookup"><span data-stu-id="7a165-231">Make a request</span></span>

<span data-ttu-id="7a165-232">Utilisez les actions de fragment de code précédent, l’application récupère la liste des projets dans le compte spécifié sur le site d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="7a165-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="7a165-233">Le ProjectContext est spécifiée pour les projets à la liste.</span><span class="sxs-lookup"><span data-stu-id="7a165-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="7a165-234">Spécifiez l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7a165-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="7a165-235">En indiquant seulement la collection, le serveur récupère la collection de projet, remplir chaque projet avec des valeurs pour le jeu de propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a165-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="7a165-236">Accès aux propriétés qui font partie du jeu de propriétés par défaut donne les résultats.</span><span class="sxs-lookup"><span data-stu-id="7a165-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="7a165-237">Accéder aux propriétés qui ne font pas partie de la valeur par défaut de définir les résultats dans une exception « Non initialisé ».</span><span class="sxs-lookup"><span data-stu-id="7a165-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="7a165-238">Chargez la demande (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="7a165-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="7a165-239">Cela fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="7a165-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="7a165-240">Exécuter la requête (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="7a165-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="7a165-241">Récupérer des informations de haut niveau du projet</span><span class="sxs-lookup"><span data-stu-id="7a165-241">Retrieve high-level project information</span></span>

<span data-ttu-id="7a165-242">Propriétés qui ne sont pas des propriétés par défaut doivent être spécifiées dans la demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="7a165-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="7a165-243">Le fragment de code suivant charge le contexte de la collection projects comme dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="7a165-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="7a165-244">Ensuite, la spécification demande des propriétés supplémentaires non par défaut à inclure dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="7a165-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="7a165-245">L’instruction load Spécifie le contexte de collection de projets et ajoute la date de début, Phase et étape le résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="7a165-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="7a165-246">Les propriétés supplémentaires peuvent être scalaires, objets et collections.</span><span class="sxs-lookup"><span data-stu-id="7a165-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="7a165-247">Éléments scalaires sont accessibles directement.</span><span class="sxs-lookup"><span data-stu-id="7a165-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="7a165-248">Objets et collections nécessitent un traitement supplémentaire, comme dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a165-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
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

<span data-ttu-id="7a165-249">Sortie d’abord trois projets :</span><span class="sxs-lookup"><span data-stu-id="7a165-249">Output of the first three projects:</span></span>
  
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

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="7a165-250">Récupérer toutes les tâches dans un projet</span><span class="sxs-lookup"><span data-stu-id="7a165-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="7a165-251">Chaque projet comporte de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="7a165-251">Each project has many tasks.</span></span> <span data-ttu-id="7a165-252">Par conséquent, extraire les tâches pour un seul projet comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="7a165-253">Établir le contexte de la collection de projets.</span><span class="sxs-lookup"><span data-stu-id="7a165-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="7a165-254">Récupérer les informations de projet, y compris les propriétés de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7a165-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="7a165-255">Notez que l’application de gestion de projets publiés.</span><span class="sxs-lookup"><span data-stu-id="7a165-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="7a165-256">Le contexte du projet publié en cours est pubProj.</span><span class="sxs-lookup"><span data-stu-id="7a165-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="7a165-257">Établir le contexte de la collection Tasks.</span><span class="sxs-lookup"><span data-stu-id="7a165-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="7a165-258">Le `pubProj.Tasks` propriété référence les tâches du projet publié en cours.</span><span class="sxs-lookup"><span data-stu-id="7a165-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="7a165-259">Charger les spécifications pour récupérer la collection de tâches, y compris les propriétés par défaut appropriées.</span><span class="sxs-lookup"><span data-stu-id="7a165-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="7a165-260">Exécuter la requête pour récupérer la collection de tâches avec les propriétés appropriées.</span><span class="sxs-lookup"><span data-stu-id="7a165-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="7a165-261">Les informations sont maintenant locales.</span><span class="sxs-lookup"><span data-stu-id="7a165-261">The information is now local.</span></span> <span data-ttu-id="7a165-262">Le fragment de code suivant traite de la collection tasks publié en écrivant les informations sur la console.</span><span class="sxs-lookup"><span data-stu-id="7a165-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
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

<span data-ttu-id="7a165-263">Sortie de tâches pour un projet :</span><span class="sxs-lookup"><span data-stu-id="7a165-263">Output of tasks for one project:</span></span>
  
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

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="7a165-264">Informations d’accès à plusieurs niveaux</span><span class="sxs-lookup"><span data-stu-id="7a165-264">Access information at multiple levels</span></span>

<span data-ttu-id="7a165-265">Chaque tâche peut avoir une ou plusieurs personnes (également appelé</span><span class="sxs-lookup"><span data-stu-id="7a165-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="7a165-266">ressources) contribuer à son exécution.</span><span class="sxs-lookup"><span data-stu-id="7a165-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="7a165-267">Les collections affectations et ressources contiennent ces informations pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="7a165-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="7a165-268">Le traitement comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="7a165-269">Obtention d’un contexte pour la tâche du projet.</span><span class="sxs-lookup"><span data-stu-id="7a165-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="7a165-270">Créer une demande et chargez la demande pour les affectations de lié à la tâche.</span><span class="sxs-lookup"><span data-stu-id="7a165-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="7a165-271">Exécuter la requête pour les affectations.</span><span class="sxs-lookup"><span data-stu-id="7a165-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="7a165-272">Créer une demande et chargez la demande pour la ressource associée à une affectation spécifique.</span><span class="sxs-lookup"><span data-stu-id="7a165-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="7a165-273">Exécuter la requête pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="7a165-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="7a165-274">La collection Assignments est demandée explicitement les informations à partir du serveur, car il n’est pas une propriété par défaut de la collection Tasks.</span><span class="sxs-lookup"><span data-stu-id="7a165-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="7a165-275">En tant que collection, une requête ultérieure est effectuée pour extraire la collection à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="7a165-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="7a165-276">La ressource est un objet.</span><span class="sxs-lookup"><span data-stu-id="7a165-276">The Resource is an object.</span></span> <span data-ttu-id="7a165-277">La requête pour une affectation inclut le nom de ressource associé à l’affectation.</span><span class="sxs-lookup"><span data-stu-id="7a165-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
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

<span data-ttu-id="7a165-278">Sortie pour les tâches 52, 75 et 76 d’un projet :</span><span class="sxs-lookup"><span data-stu-id="7a165-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
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

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="7a165-279">Champs de niveau entreprise personnalisés Access</span><span class="sxs-lookup"><span data-stu-id="7a165-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="7a165-280">Il existe des champs personnalisés pour Project Online.</span><span class="sxs-lookup"><span data-stu-id="7a165-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="7a165-281">Il s’agit des champs de niveau entreprise qui peuvent être associés à des projets individuels.</span><span class="sxs-lookup"><span data-stu-id="7a165-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="7a165-282">Cette section décrit comment accéder à ces champs.</span><span class="sxs-lookup"><span data-stu-id="7a165-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="7a165-283">Champs personnalisés ne sont pas inclus dans le jeu de propriétés associées à un projet par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a165-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="7a165-284">Ainsi, ils doivent identification explicite de la spécification de récupération.</span><span class="sxs-lookup"><span data-stu-id="7a165-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="7a165-285">La vue de haut niveau du processus se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a165-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="7a165-286">Tunnel pour le champ personnalisé à l’aide de son nom commun.</span><span class="sxs-lookup"><span data-stu-id="7a165-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="7a165-287">Récupérez le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7a165-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="7a165-288">Revenez au contexte global et interroger le système en utilisant le nom interne du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7a165-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="7a165-289">Tunnel au champ personnalisé et récupérer son nom interne utilisé pour le système de requête</span><span class="sxs-lookup"><span data-stu-id="7a165-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="7a165-290">Cette tâche spécifie une récupération qui utilise une propriété par défaut avec un détail ajouté.</span><span class="sxs-lookup"><span data-stu-id="7a165-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="7a165-291">Commencez par utiliser le contexte de projets, comme décrit au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="7a165-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="7a165-292">Ajoutez deux éléments à la demande de récupération de collection projets en plus de toutes les autres propriétés par défaut pour récupérer :</span><span class="sxs-lookup"><span data-stu-id="7a165-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="7a165-293">Le `p => p.IncludeCustomFields` clause identifie la nécessité d’utiliser un objet project qui prend en charge les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7a165-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="7a165-294">Le `p => p.IncludeCustomFields.CustomFields` clause demande l’inclusion de données de champ personnalisé dans le résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="7a165-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="7a165-295">Cette information est utilisée après que le nom interne de champ personnalisé est extrait.</span><span class="sxs-lookup"><span data-stu-id="7a165-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="7a165-296">Charger à la demande.</span><span class="sxs-lookup"><span data-stu-id="7a165-296">Load the request.</span></span>
    
   <span data-ttu-id="7a165-297">Cela fait partie de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="7a165-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="7a165-298">Exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="7a165-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="7a165-299">Ces informations sur le client, de créer une demande pour récupérer les champs personnalisés associés au projet actuel.</span><span class="sxs-lookup"><span data-stu-id="7a165-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="7a165-300">Recherchez les champs personnalisés appropriée et extraire le nom interne du champ.</span><span class="sxs-lookup"><span data-stu-id="7a165-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="7a165-301">Le nom interne du champ personnalisé est extrait.</span><span class="sxs-lookup"><span data-stu-id="7a165-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="7a165-302">Éléments de haut niveau 1 et 2 sont maintenant terminées.</span><span class="sxs-lookup"><span data-stu-id="7a165-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="7a165-303">Retournez dans le contexte du projet et récupérer la valeur du champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7a165-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="7a165-304">La valeur du champ personnalisé est extraite en utilisant le nom interne sous forme d’index.</span><span class="sxs-lookup"><span data-stu-id="7a165-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="7a165-305">Sortie de trois projets constituée de l’ID de projet, nom du projet, nom de champ personnalisé, nom interne de champ personnalisé et valeur de champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7a165-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="7a165-306">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a165-306">See also</span></span>

<span data-ttu-id="7a165-307">Pour la documentation et des exemples relatifs à Project Online et développement d’applications à l’aide de CSOM, voir le [Portail de développement Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="7a165-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

