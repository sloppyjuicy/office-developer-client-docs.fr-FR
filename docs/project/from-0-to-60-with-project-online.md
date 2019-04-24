---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: "Un développeur d'applications peut personnaliser un site Project Online (SharePoint hébergé) à l'aide d'applications autonomes et/ou de compléments de projet. Il est possible d'effectuer une multitude d'applications entre les besoins des utilisateurs impliqués dans un projet et les fonctions de prise en charge de PMO, tels que les suivants:"
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344407"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="53138-103">De 0 à 60 avec Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="53138-104">Un développeur d'applications peut personnaliser un site Project Online (SharePoint hébergé) à l'aide d'applications autonomes et/ou de compléments de projet. Il est possible d'effectuer une multitude d'applications entre les besoins des utilisateurs impliqués dans un projet et les fonctions de prise en charge de PMO, tels que les suivants:</span><span class="sxs-lookup"><span data-stu-id="53138-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="53138-105">Entrée de données de la fiche de pointage rationalisée pour les travailleurs</span><span class="sxs-lookup"><span data-stu-id="53138-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="53138-106">Approbation de la fiche de pointage efficace pour les superviseurs</span><span class="sxs-lookup"><span data-stu-id="53138-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="53138-107">Supervision des autorisations (approvisionnement et état) nécessaires pour un projet</span><span class="sxs-lookup"><span data-stu-id="53138-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="53138-108">État/contrôle d'intégrité des projets actifs</span><span class="sxs-lookup"><span data-stu-id="53138-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="53138-109">Rapport des problèmes</span><span class="sxs-lookup"><span data-stu-id="53138-109">Issues report</span></span>
- <span data-ttu-id="53138-110">Modifier le rapport d'état de gestion</span><span class="sxs-lookup"><span data-stu-id="53138-110">Change Management Status report</span></span>
    
<span data-ttu-id="53138-111">Project Online inclut une prise en charge des API pour les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="53138-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="53138-112">Pour un complément hébergé par un projet (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="53138-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="53138-113">Code (JavaScript, HTML, CSS) hébergé dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="53138-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="53138-114">Les ressources qui sont téléchargées vers le navigateur et exécutées sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="53138-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="53138-115">Logique métier en JavaScript</span><span class="sxs-lookup"><span data-stu-id="53138-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="53138-116">Accédez aux données stockées dans Project Online ou dans SharePoint, par exemple (sans s'y limiter):</span><span class="sxs-lookup"><span data-stu-id="53138-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="53138-117">Champs personnalisés</span><span class="sxs-lookup"><span data-stu-id="53138-117">Custom fields</span></span>  
  - <span data-ttu-id="53138-118">Listes</span><span class="sxs-lookup"><span data-stu-id="53138-118">Lists</span></span>
    
- <span data-ttu-id="53138-119">Pour un complément Project (SharePoint) hébergé par un fournisseur:</span><span class="sxs-lookup"><span data-stu-id="53138-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="53138-120">Code qui existe sur un site externe au site Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="53138-121">Un site externe, qui peut être (sans s'y limiter):</span><span class="sxs-lookup"><span data-stu-id="53138-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="53138-122">Un autre site SharePoint</span><span class="sxs-lookup"><span data-stu-id="53138-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="53138-123">Application/service Web bâti sur n'importe quelle plateforme</span><span class="sxs-lookup"><span data-stu-id="53138-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="53138-124">Le site externe contient une logique métier</span><span class="sxs-lookup"><span data-stu-id="53138-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="53138-125">Le navigateur est redirigé de Project Online vers le site externe avec des jetons d'accès à Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="53138-126">Le site externe peut effectuer des appels vers SharePoint et Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="53138-127">Pour un complément externe/autonome:</span><span class="sxs-lookup"><span data-stu-id="53138-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="53138-128">L'utilisateur exécute une application sur son appareil</span><span class="sxs-lookup"><span data-stu-id="53138-128">User executes an application on their device</span></span>
  - <span data-ttu-id="53138-129">L'application authentifie et appelle directement les API Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="53138-130">Type d’application</span><span class="sxs-lookup"><span data-stu-id="53138-130">Type of application</span></span>|<span data-ttu-id="53138-131">Implémentation de l'API</span><span class="sxs-lookup"><span data-stu-id="53138-131">API implementation</span></span>|<span data-ttu-id="53138-132">Environnement cible</span><span class="sxs-lookup"><span data-stu-id="53138-132">Target environment</span></span>|<span data-ttu-id="53138-133">Exemples d'applications</span><span class="sxs-lookup"><span data-stu-id="53138-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53138-134">Projet hébergé</span><span class="sxs-lookup"><span data-stu-id="53138-134">Project hosted</span></span>  <br/> |<span data-ttu-id="53138-135">JSOM (modèle objet de script Java)</span><span class="sxs-lookup"><span data-stu-id="53138-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="53138-136">REST</span><span class="sxs-lookup"><span data-stu-id="53138-136">REST</span></span>  <br/> |<span data-ttu-id="53138-137">Navigateur</span><span class="sxs-lookup"><span data-stu-id="53138-137">Browser</span></span>  <br/> |<span data-ttu-id="53138-138">Entrée de la ligne de présence</span><span class="sxs-lookup"><span data-stu-id="53138-138">Timecard entry</span></span>  <br/> <span data-ttu-id="53138-139">Approbation de la fiche de pointage</span><span class="sxs-lookup"><span data-stu-id="53138-139">Timecard approval</span></span>  <br/> <span data-ttu-id="53138-140">État du projet</span><span class="sxs-lookup"><span data-stu-id="53138-140">Project Status</span></span>  <br/> <span data-ttu-id="53138-141">Rapport des problèmes</span><span class="sxs-lookup"><span data-stu-id="53138-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="53138-142">Fournisseur de projets hébergé</span><span class="sxs-lookup"><span data-stu-id="53138-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="53138-143">Bibliothèque cliente CSOM</span><span class="sxs-lookup"><span data-stu-id="53138-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="53138-144">Site Web/application Azure</span><span class="sxs-lookup"><span data-stu-id="53138-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="53138-145">Environnement non-Windows (lampe, etc.)</span><span class="sxs-lookup"><span data-stu-id="53138-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="53138-146">Validateur de feuille de temps externe</span><span class="sxs-lookup"><span data-stu-id="53138-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="53138-147">Importateur de projet</span><span class="sxs-lookup"><span data-stu-id="53138-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="53138-148">Externe/autonome</span><span class="sxs-lookup"><span data-stu-id="53138-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="53138-149">REST</span><span class="sxs-lookup"><span data-stu-id="53138-149">REST</span></span>  <br/> <span data-ttu-id="53138-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="53138-150">CSOM</span></span>  <br/> |<span data-ttu-id="53138-151">REST: n'importe quelle plateforme</span><span class="sxs-lookup"><span data-stu-id="53138-151">REST - any platform</span></span>  <br/> <span data-ttu-id="53138-152">CSOM: toute plateforme prise en charge par .NET</span><span class="sxs-lookup"><span data-stu-id="53138-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="53138-153">Entrée de la ligne de présence</span><span class="sxs-lookup"><span data-stu-id="53138-153">Timecard entry</span></span>  <br/> <span data-ttu-id="53138-154">Migration de projets vers un nouveau site</span><span class="sxs-lookup"><span data-stu-id="53138-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="53138-155">Modifier l'état de gestion.</span><span class="sxs-lookup"><span data-stu-id="53138-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="53138-156">Que faut-il prendre pour commencer à développer des applications pour Project Online?</span><span class="sxs-lookup"><span data-stu-id="53138-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="53138-157">Les éléments communs nécessaires au développement d'applications Project Online sont un compte Project Online et des données de test: des projets et des informations relatives au projet qui incluent des affectations, des tâches, des ressources et des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="53138-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="53138-158">Un environnement de développement est également nécessaire, mais des caractéristiques de l'environnement de développement dépendent du type d'application et de l'interface API nécessaires pour l'application.</span><span class="sxs-lookup"><span data-stu-id="53138-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="53138-159">Les sections suivantes décrivent les besoins de développement pour les trois interfaces API.</span><span class="sxs-lookup"><span data-stu-id="53138-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="53138-160">La documentation de référence décrit le modèle objet qui est commun aux trois interfaces, ainsi qu'un mappage d'entité qui affiche les relations entre les composants de modèle objet.</span><span class="sxs-lookup"><span data-stu-id="53138-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="53138-161">Environnement de développement de complément hébergé par le projet</span><span class="sxs-lookup"><span data-stu-id="53138-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="53138-162">Un complément hébergé est un complément qui réside sur le serveur et téléchargé dans un navigateur pour l'exécution de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="53138-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="53138-163">Les compléments hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="53138-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="53138-164">Project Online fournit des références à la bibliothèque JSOM pour l'exécution de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="53138-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="53138-165">En supposant que le développement se trouve sur une plateforme Windows, les ressources nécessaires sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="53138-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="53138-166">Visual Studio 2015 (recommandé) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="53138-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="53138-167">Outils de développement Office pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="53138-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="53138-168">Langage JavaScript</span><span class="sxs-lookup"><span data-stu-id="53138-168">JavaScript language</span></span>
    
<span data-ttu-id="53138-169">Consultez https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages l'exemple d'application.</span><span class="sxs-lookup"><span data-stu-id="53138-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="53138-170">Vous pouvez télécharger et exécuter l'exemple en quelques étapes simples:</span><span class="sxs-lookup"><span data-stu-id="53138-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="53138-171">Télécharger et ouvrir l'exemple d'application</span><span class="sxs-lookup"><span data-stu-id="53138-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="53138-172">Mettre à jour la propriété SiteURL dans la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="53138-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="53138-173">Project Online examine à la fois l'étendue de l'application du complément et les autorisations de l'utilisateur pour régir l'accès aux informations sur l'hôte Project online.</span><span class="sxs-lookup"><span data-stu-id="53138-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="53138-174">Si l'accès est explicitement refusé dans l'un ou l'autre de ces paramètres, ou les deux, Project Online refuse l'accès aux informations.</span><span class="sxs-lookup"><span data-stu-id="53138-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="53138-175">Dans le cas contraire, l'accès est accordé.</span><span class="sxs-lookup"><span data-stu-id="53138-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="53138-176">Activez [chargement](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.</span><span class="sxs-lookup"><span data-stu-id="53138-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="53138-177">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-177">Build the project.</span></span>
    
5. <span data-ttu-id="53138-178">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="53138-179">Environnement de développement de complément hébergé par un fournisseur de projets</span><span class="sxs-lookup"><span data-stu-id="53138-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="53138-180">Les compléments hébergés par le fournisseur sont des applications écrites et résidant sur n'importe quelle plateforme Web.</span><span class="sxs-lookup"><span data-stu-id="53138-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="53138-181">Ils peuvent se connecter et effectuer des opérations de données à l'aide de l'API REST (ou CSOM pour les plateformes Microsoft).</span><span class="sxs-lookup"><span data-stu-id="53138-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="53138-182">Toute langue et tout environnement qui prend en charge l'interface REST peuvent être utilisés pour le développement.</span><span class="sxs-lookup"><span data-stu-id="53138-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="53138-183">Un exemple de l'environnement de développement Windows pour ce type d'application inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="53138-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="53138-184">Visual Studio 2015 (recommandé) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="53138-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="53138-185">Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="53138-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="53138-186">.NET Framework 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53138-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="53138-187">[Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM)</span><span class="sxs-lookup"><span data-stu-id="53138-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="53138-188">Langage de programmation, tel que C#</span><span class="sxs-lookup"><span data-stu-id="53138-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="53138-189">Visitez https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations les exemples de scripts de travail.</span><span class="sxs-lookup"><span data-stu-id="53138-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="53138-190">Vous pouvez exécuter l'exemple en quelques étapes:</span><span class="sxs-lookup"><span data-stu-id="53138-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="53138-191">Télécharger et ouvrir l'exemple d'application</span><span class="sxs-lookup"><span data-stu-id="53138-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="53138-192">Mettre à jour la propriété SiteURL dans la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="53138-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="53138-193">Project Online examine à la fois l'étendue de l'application du complément et les autorisations de l'utilisateur pour régir l'accès aux informations sur l'hôte Project online.</span><span class="sxs-lookup"><span data-stu-id="53138-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="53138-194">Si l'accès est explicitement refusé dans l'un ou l'autre de ces paramètres, ou les deux, Project Online refuse l'accès aux informations.</span><span class="sxs-lookup"><span data-stu-id="53138-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="53138-195">Dans le cas contraire, l'accès est accordé.</span><span class="sxs-lookup"><span data-stu-id="53138-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="53138-196">Activez [chargement](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.</span><span class="sxs-lookup"><span data-stu-id="53138-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="53138-197">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-197">Build the project.</span></span>
    
5. <span data-ttu-id="53138-198">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="53138-199">Environnement de développement d'application externe/autonome</span><span class="sxs-lookup"><span data-stu-id="53138-199">External/standalone application development environment</span></span>

<span data-ttu-id="53138-200">Une application autonome peut appeler Project Online à l'aide du modèle objet côté client (CSOM) ou REST pour communiquer avec Project Online pour créer, récupérer, mettre à jour et supprimer des informations résidant sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="53138-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="53138-201">Il s'agit d'une application cliente autonome qui dépend du niveau d'accès utilisateur à exécuter.</span><span class="sxs-lookup"><span data-stu-id="53138-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="53138-202">Un exemple de l'environnement de développement Windows pour ce type d'application inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="53138-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="53138-203">Visual Studio 2015 (recommandé) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="53138-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="53138-204">Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="53138-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="53138-205">.NET Framework 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53138-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="53138-206">[Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM)</span><span class="sxs-lookup"><span data-stu-id="53138-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="53138-207">Langage de programmation, tel que C#</span><span class="sxs-lookup"><span data-stu-id="53138-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="53138-208">Consultez https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields l'exemple d'application.</span><span class="sxs-lookup"><span data-stu-id="53138-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="53138-209">Vous pouvez exécuter l'exemple en quelques étapes:</span><span class="sxs-lookup"><span data-stu-id="53138-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="53138-210">Télécharger l'exemple d'application</span><span class="sxs-lookup"><span data-stu-id="53138-210">Download the sample application</span></span>
    
2. <span data-ttu-id="53138-211">Effectuez quelques modifications pour accéder à votre site Project Online: le nom du site, le compte d'utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="53138-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="53138-212">Assurez-vous que l'utilisateur a accès à tous les projets.</span><span class="sxs-lookup"><span data-stu-id="53138-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="53138-213">Project Online utilise les autorisations des utilisateurs pour régir l'accès aux informations dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="53138-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="53138-214">Ajoutez l'assembly SharePoint aux références à l'aide de la console du gestionnaire de package NuGet, accessible à partir du menu outils en tapant ce qui suit dans la console NuGet:</span><span class="sxs-lookup"><span data-stu-id="53138-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="53138-215">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-215">Build the project.</span></span>
    
5. <span data-ttu-id="53138-216">Exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="53138-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="53138-217">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="53138-217">Next steps</span></span>

<span data-ttu-id="53138-218">Chaque exemple d'application contient un article expliquant les points forts de l'utilisation de l'API de projet individuelle.</span><span class="sxs-lookup"><span data-stu-id="53138-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="53138-219">Les articles figurent dans la liste suivante, ainsi que quelques articles qui décrivent les relations entre les entités, les informations sur le système de requêtes et l'accès aux champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="53138-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="53138-220">Développement d'une application Project Online à l'aide du modèle objet côté client</span><span class="sxs-lookup"><span data-stu-id="53138-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="53138-221">Développement d'un complément Project Online à l'aide du modèle objet JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="53138-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="53138-222">Accès aux champs personnalisés d’entreprise Project Online</span><span class="sxs-lookup"><span data-stu-id="53138-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="53138-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53138-223">See also</span></span>

<span data-ttu-id="53138-224">Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="53138-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

