---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un développeur d’applications peut personnaliser un site Project Online (hébergé SharePoint) à l’aide d’applications autonomes et/ou de Project de sites. Un grand nombre d’applications sont possibles, qu’il s’agit de répondre aux besoins de ceux impliqués dans un projet ou de fonctions de prise en charge PMO, telles que l’une des suivantes :'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344407"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="b6ea1-103">De 0 à 60 avec Project Online</span><span class="sxs-lookup"><span data-stu-id="b6ea1-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="b6ea1-104">Un développeur d’applications peut personnaliser un site Project Online (hébergé SharePoint) à l’aide d’applications autonomes et/ou de Project de sites. Un grand nombre d’applications sont possibles, qu’il s’agit de répondre aux besoins de ceux impliqués dans un projet ou de fonctions de prise en charge PMO, telles que l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="b6ea1-105">Entrée simplifiée des données de carte de temps pour les employés</span><span class="sxs-lookup"><span data-stu-id="b6ea1-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="b6ea1-106">Approbation de carte de temps efficace pour les superviseurs</span><span class="sxs-lookup"><span data-stu-id="b6ea1-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="b6ea1-107">Supervision des autorisations (approvisionnement et état) nécessaires pour un projet</span><span class="sxs-lookup"><span data-stu-id="b6ea1-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="b6ea1-108">Vérification de l’état/de l’état des projets actifs</span><span class="sxs-lookup"><span data-stu-id="b6ea1-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="b6ea1-109">Rapport des problèmes</span><span class="sxs-lookup"><span data-stu-id="b6ea1-109">Issues report</span></span>
- <span data-ttu-id="b6ea1-110">Rapport d’état de la gestion des changements</span><span class="sxs-lookup"><span data-stu-id="b6ea1-110">Change Management Status report</span></span>
    
<span data-ttu-id="b6ea1-111">Project Online la prise en charge de l’API pour prendre en charge les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="b6ea1-112">Pour un Project (SharePoint) hébergé :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="b6ea1-113">Code (JavaScript, HTML, CSS) hébergé dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b6ea1-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="b6ea1-114">Ressources téléchargées dans le navigateur et exécutées sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="b6ea1-115">Logique métier en JavaScript</span><span class="sxs-lookup"><span data-stu-id="b6ea1-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="b6ea1-116">Accéder aux données qui sont dans/stockées dans Project Online ou SharePoint par exemple (mais n’est pas limité à) :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="b6ea1-117">Champs personnalisés</span><span class="sxs-lookup"><span data-stu-id="b6ea1-117">Custom fields</span></span>  
  - <span data-ttu-id="b6ea1-118">Listes</span><span class="sxs-lookup"><span data-stu-id="b6ea1-118">Lists</span></span>
    
- <span data-ttu-id="b6ea1-119">Pour un Project (SharePoint) hébergé par un fournisseur :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="b6ea1-120">Code qui existe sur un site externe au site Project Online site</span><span class="sxs-lookup"><span data-stu-id="b6ea1-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="b6ea1-121">Un site externe, qui peut être (mais n’est pas limité à) :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="b6ea1-122">Autre site SharePoint site</span><span class="sxs-lookup"><span data-stu-id="b6ea1-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="b6ea1-123">Application web/service créé sur n’importe quelle plateforme</span><span class="sxs-lookup"><span data-stu-id="b6ea1-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="b6ea1-124">Le site externe contient une logique métier</span><span class="sxs-lookup"><span data-stu-id="b6ea1-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="b6ea1-125">Le navigateur est redirigé de Project Online vers un site externe avec des jetons d’accès Project Online</span><span class="sxs-lookup"><span data-stu-id="b6ea1-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="b6ea1-126">Le site externe peut effectuer des appels vers SharePoint et Project Online</span><span class="sxs-lookup"><span data-stu-id="b6ea1-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="b6ea1-127">Pour un add-in externe/autonome :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="b6ea1-128">Un utilisateur exécute une application sur son appareil</span><span class="sxs-lookup"><span data-stu-id="b6ea1-128">User executes an application on their device</span></span>
  - <span data-ttu-id="b6ea1-129">L’application s’authentifier et appelle Project Online API directement</span><span class="sxs-lookup"><span data-stu-id="b6ea1-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="b6ea1-130">Type d’application</span><span class="sxs-lookup"><span data-stu-id="b6ea1-130">Type of application</span></span>|<span data-ttu-id="b6ea1-131">Implémentation d’API</span><span class="sxs-lookup"><span data-stu-id="b6ea1-131">API implementation</span></span>|<span data-ttu-id="b6ea1-132">Environnement cible</span><span class="sxs-lookup"><span data-stu-id="b6ea1-132">Target environment</span></span>|<span data-ttu-id="b6ea1-133">Exemples d’applications</span><span class="sxs-lookup"><span data-stu-id="b6ea1-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b6ea1-134">Project hébergé</span><span class="sxs-lookup"><span data-stu-id="b6ea1-134">Project hosted</span></span>  <br/> |<span data-ttu-id="b6ea1-135">JSOM (Java Script Object Model)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="b6ea1-136">REST</span><span class="sxs-lookup"><span data-stu-id="b6ea1-136">REST</span></span>  <br/> |<span data-ttu-id="b6ea1-137">Navigateur</span><span class="sxs-lookup"><span data-stu-id="b6ea1-137">Browser</span></span>  <br/> |<span data-ttu-id="b6ea1-138">Entrée de carte de temps</span><span class="sxs-lookup"><span data-stu-id="b6ea1-138">Timecard entry</span></span>  <br/> <span data-ttu-id="b6ea1-139">Approbation de carte de temps</span><span class="sxs-lookup"><span data-stu-id="b6ea1-139">Timecard approval</span></span>  <br/> <span data-ttu-id="b6ea1-140">État du projet</span><span class="sxs-lookup"><span data-stu-id="b6ea1-140">Project Status</span></span>  <br/> <span data-ttu-id="b6ea1-141">Rapport des problèmes</span><span class="sxs-lookup"><span data-stu-id="b6ea1-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="b6ea1-142">Project Fournisseur hébergé</span><span class="sxs-lookup"><span data-stu-id="b6ea1-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="b6ea1-143">Bibliothèque cliente CSOM</span><span class="sxs-lookup"><span data-stu-id="b6ea1-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="b6ea1-144">Site web/application Azure</span><span class="sxs-lookup"><span data-stu-id="b6ea1-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="b6ea1-145">Environnement non Windows (LAMP, etc.)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="b6ea1-146">Validateur de feuille de temps externe</span><span class="sxs-lookup"><span data-stu-id="b6ea1-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="b6ea1-147">Project Importer</span><span class="sxs-lookup"><span data-stu-id="b6ea1-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="b6ea1-148">Externe/Autonome</span><span class="sxs-lookup"><span data-stu-id="b6ea1-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="b6ea1-149">REST</span><span class="sxs-lookup"><span data-stu-id="b6ea1-149">REST</span></span>  <br/> <span data-ttu-id="b6ea1-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="b6ea1-150">CSOM</span></span>  <br/> |<span data-ttu-id="b6ea1-151">REST - n’importe quelle plateforme</span><span class="sxs-lookup"><span data-stu-id="b6ea1-151">REST - any platform</span></span>  <br/> <span data-ttu-id="b6ea1-152">CSOM : toute plateforme prise en charge par .NET</span><span class="sxs-lookup"><span data-stu-id="b6ea1-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="b6ea1-153">Entrée de carte de temps</span><span class="sxs-lookup"><span data-stu-id="b6ea1-153">Timecard entry</span></span>  <br/> <span data-ttu-id="b6ea1-154">Migration de projets vers un nouveau site</span><span class="sxs-lookup"><span data-stu-id="b6ea1-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="b6ea1-155">État de gestion des changements.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="b6ea1-156">Que faut-il pour commencer à développer des applications pour Project Online ?</span><span class="sxs-lookup"><span data-stu-id="b6ea1-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="b6ea1-157">Les éléments courants nécessaires au développement d’applications Project Online sont un compte Project Online et des données de test , des projets et des informations relatives aux projets qui incluent des affectations, des tâches, des ressources et des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="b6ea1-158">Un environnement de développement est également nécessaire, mais les spécificités de l’environnement de développement dépendent du type d’application et de l’interface API nécessaires pour l’application.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="b6ea1-159">Les sections suivantes décrivent les besoins de développement pour les trois interfaces API.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="b6ea1-160">La documentation de référence décrit le modèle objet commun aux trois interfaces, ainsi qu’une carte d’entité qui illustre les relations entre les composants du modèle objet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="b6ea1-161">Project environnement de développement de add-in hébergé</span><span class="sxs-lookup"><span data-stu-id="b6ea1-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="b6ea1-162">Un add-in hébergé est un module qui réside sur le serveur et qui est téléchargé dans un navigateur pour exécution.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="b6ea1-163">Les add-ins hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="b6ea1-164">Project Online fournit des références à la bibliothèque JSOM pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="b6ea1-165">En supposant que le développement se trouve sur une plateforme Windows, les ressources nécessaires suivent :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="b6ea1-166">Visual Studio 2015 (de préférence) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="b6ea1-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="b6ea1-167">Office de développement pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6ea1-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="b6ea1-168">Langage JavaScript</span><span class="sxs-lookup"><span data-stu-id="b6ea1-168">JavaScript language</span></span>
    
<span data-ttu-id="b6ea1-169">Visitez https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages un exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="b6ea1-170">Vous pouvez télécharger et exécuter l’exemple en quelques étapes simples :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="b6ea1-171">Télécharger et ouvrir l’exemple d’application</span><span class="sxs-lookup"><span data-stu-id="b6ea1-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="b6ea1-172">Mettre à jour siteURL dans la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6ea1-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="b6ea1-173">Project Online examine à la fois l’étendue de l’application du module complémentaire et les autorisations de l’utilisateur pour régir l’accès aux informations sur l Project Online hôte.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="b6ea1-174">Si l’accès est explicitement refusé dans l’un des paramètres ou les deux, Project Online refuse l’accès aux informations.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="b6ea1-175">Sinon, l’accès est accordé.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="b6ea1-176">Activez [le chargement de version secondaire](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="b6ea1-177">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-177">Build the project.</span></span>
    
5. <span data-ttu-id="b6ea1-178">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="b6ea1-179">Project environnement de développement de add-in hébergé par un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b6ea1-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="b6ea1-180">Les applications hébergées par un fournisseur sont des applications écrites et résidant sur n’importe quelle plateforme web.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="b6ea1-181">Ils peuvent se connecter et effectuer des opérations de données à l’aide de l’API REST (ou CSOM pour les plateformes Microsoft).</span><span class="sxs-lookup"><span data-stu-id="b6ea1-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="b6ea1-182">Tout langage et environnement qui prend en charge l’interface REST peut être utilisé pour le développement.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="b6ea1-183">Un exemple de l’environnement Windows de développement pour ce type d’application comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="b6ea1-184">Visual Studio 2015 (de préférence) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="b6ea1-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="b6ea1-185">Microsoft Office Outils de développement Visual Studio (fournis avec Visual Studio 2015 Professional et Enterprise éditions)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="b6ea1-186">.NET Framework 4.0 ou plus</span><span class="sxs-lookup"><span data-stu-id="b6ea1-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="b6ea1-187">[Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="b6ea1-188">Langage de programmation, tel que C #</span><span class="sxs-lookup"><span data-stu-id="b6ea1-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="b6ea1-189">Consultez https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations les exemples de scripts de travail.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="b6ea1-190">Vous pouvez exécuter l’exemple en quelques étapes :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="b6ea1-191">Télécharger et ouvrir l’exemple d’application</span><span class="sxs-lookup"><span data-stu-id="b6ea1-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="b6ea1-192">Mettre à jour siteURL dans la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6ea1-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="b6ea1-193">Project Online examine à la fois l’étendue de l’application du module complémentaire et les autorisations de l’utilisateur pour régir l’accès aux informations sur l Project Online hôte.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="b6ea1-194">Si l’accès est explicitement refusé dans l’un des paramètres ou les deux, Project Online refuse l’accès aux informations.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="b6ea1-195">Sinon, l’accès est accordé.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="b6ea1-196">Activez [le chargement de version secondaire](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="b6ea1-197">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-197">Build the project.</span></span>
    
5. <span data-ttu-id="b6ea1-198">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="b6ea1-199">Environnement de développement d’applications externes/autonomes</span><span class="sxs-lookup"><span data-stu-id="b6ea1-199">External/standalone application development environment</span></span>

<span data-ttu-id="b6ea1-200">Une application autonome peut appeler Project Online à l’aide du modèle objet côté client (CSOM) ou REST pour communiquer avec Project Online afin de créer, récupérer, mettre à jour et supprimer des informations résidant sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="b6ea1-201">Il s’agit d’une application cliente autonome qui dépend du niveau d’accès utilisateur à exécuter.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="b6ea1-202">Un exemple de l’environnement Windows de développement pour ce type d’application comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="b6ea1-203">Visual Studio 2015 (de préférence) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="b6ea1-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="b6ea1-204">Microsoft Office Outils de développement Visual Studio (fournis avec Visual Studio 2015 Professional et Enterprise éditions)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="b6ea1-205">.NET Framework 4.0 ou plus</span><span class="sxs-lookup"><span data-stu-id="b6ea1-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="b6ea1-206">[Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="b6ea1-207">Langage de programmation, tel que C #</span><span class="sxs-lookup"><span data-stu-id="b6ea1-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="b6ea1-208">Visitez https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields un exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="b6ea1-209">Vous pouvez exécuter l’exemple en quelques étapes :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="b6ea1-210">Télécharger l’exemple d’application</span><span class="sxs-lookup"><span data-stu-id="b6ea1-210">Download the sample application</span></span>
    
2. <span data-ttu-id="b6ea1-211">A apporté quelques modifications pour accéder à votre site Project Online site : le nom du site, le compte d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="b6ea1-212">Assurez-vous que l’utilisateur a accès à tous les projets.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="b6ea1-213">Project Online utilise les autorisations utilisateur pour régir l’accès aux informations dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="b6ea1-214">Ajoutez l’assembly SharePoint aux références à l’aide de la console Nuget Gestionnaire de package, disponible dans le menu Outils en tapant ce qui suit dans la console Nuget :</span><span class="sxs-lookup"><span data-stu-id="b6ea1-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="b6ea1-215">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-215">Build the project.</span></span>
    
5. <span data-ttu-id="b6ea1-216">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="b6ea1-217">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b6ea1-217">Next steps</span></span>

<span data-ttu-id="b6ea1-218">Chaque exemple d’application dispose d’un article expliquant les points forts de l’utilisation de l’API Project individuelle.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="b6ea1-219">Les articles apparaissent dans la liste suivante, ainsi que quelques articles qui décrivent les relations d’entité, les informations sur le système de requête et l’accès aux champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="b6ea1-220">Développement d’une application Project Online’aide du modèle objet côté client</span><span class="sxs-lookup"><span data-stu-id="b6ea1-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="b6ea1-221">Développement d’Project Online à l’aide du modèle objet JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="b6ea1-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="b6ea1-222">Accès aux champs personnalisés d’entreprise Project Online</span><span class="sxs-lookup"><span data-stu-id="b6ea1-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="b6ea1-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6ea1-223">See also</span></span>

<span data-ttu-id="b6ea1-224">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="b6ea1-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

