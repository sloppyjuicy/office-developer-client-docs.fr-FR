---
title: Conditions préalables pour les exemples de code basés sur ASMX
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- exemples de code, serveur de projet, serveur Project, programmation,PSI, compilation d’exemples de code,PSI, programmation
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code ASMX inclus dans les rubriques de référence psi (Project Server Interface).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357079"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="9de0c-104">Conditions préalables pour les exemples de code basés sur ASMX</span><span class="sxs-lookup"><span data-stu-id="9de0c-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="9de0c-105">Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code ASMX inclus dans les rubriques de référence psi (Project Server Interface).</span><span class="sxs-lookup"><span data-stu-id="9de0c-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="9de0c-106">La plupart des exemples de code inclus dans la bibliothèque de classes et la référence de [service web Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été initialement créés pour le SDK Office Project 2007 et utilisent un format standard pour les services web ASMX.</span><span class="sxs-lookup"><span data-stu-id="9de0c-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="9de0c-107">Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu’unité complète.</span><span class="sxs-lookup"><span data-stu-id="9de0c-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="9de0c-108">Des exceptions sont notées dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="9de0c-109">Les nouveaux exemples PSI du SDK Project 2013 sont conformes à un format qui utilise les services WCF (Windows Communication Foundation).</span><span class="sxs-lookup"><span data-stu-id="9de0c-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="9de0c-110">Les exemples ASMX peuvent également être adaptés pour utiliser les services WCF.</span><span class="sxs-lookup"><span data-stu-id="9de0c-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="9de0c-111">Cet article montre comment utiliser les exemples avec les services web ASMX.</span><span class="sxs-lookup"><span data-stu-id="9de0c-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="9de0c-112">Pour plus d’informations sur l’utilisation des exemples avec les services WCF, voir [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="9de0c-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9de0c-113">L’interface de service web ASMX de la PSI déconseillé dans Project Server 2013, mais est toujours prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9de0c-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="9de0c-114">Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, de nouvelles applications doivent être développées avec le modèle CSOM.</span><span class="sxs-lookup"><span data-stu-id="9de0c-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="9de0c-115">Le CSOM permet aux applications de fonctionner avec Project Online ou une installation sur site de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="9de0c-116">Dans le cas contraire, si votre application utilise l’interface PSI, elle doit utiliser l’interface WCF, qui est la technologie recommandée pour les communications réseau.</span><span class="sxs-lookup"><span data-stu-id="9de0c-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="9de0c-117">Les applications qui utilisent l’interface ASMX ou l’interface WCF ne peuvent fonctionner que pour les installations sur site de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="9de0c-118">Pour plus d’informations sur le modèle CSOM, voir [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="9de0c-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="9de0c-119">Avant d’exécutez les exemples de code, vous devez configurer l’environnement de développement, configurer l’application et modifier les valeurs de constante génériques pour qu’elle corresponde à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="9de0c-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="9de0c-120">Configuration de l'environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9de0c-120">Setting up the development environment</span></span>
<span data-ttu-id="9de0c-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span></span>

1. <span data-ttu-id="9de0c-122">**Configurer un système de test Project Server.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="9de0c-123">Utilisez un système de test Project server chaque fois que vous développez ou testez.</span><span class="sxs-lookup"><span data-stu-id="9de0c-123">Use a test Project Server system whenever you are developing or testing.</span></span> <span data-ttu-id="9de0c-124">Même lorsque votre code fonctionne parfaitement, l’interprojet des dépendances, des rapports ou d’autres facteurs environnementaux peut entraîner des conséquences inattendues.</span><span class="sxs-lookup"><span data-stu-id="9de0c-124">Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="9de0c-125">Vérifiez que vous êtes un utilisateur valide sur le serveur et que vous avez les autorisations suffisantes pour les appels PSI que votre application utilise.</span><span class="sxs-lookup"><span data-stu-id="9de0c-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="9de0c-126">La rubrique de référence pour chaque méthode PSI inclut une table Project Server Permissions.</span><span class="sxs-lookup"><span data-stu-id="9de0c-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="9de0c-127">Par exemple, le [Project. La méthode QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l’autorisation **NewProject** globale et **l’autorisation SaveProjectTemplate.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="9de0c-128">Dans certains cas, vous de devez peut-être déboguer à distance sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9de0c-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="9de0c-129">Il se peut également que vous de dû configurer un programme de gestion d’événements en installant un assembly de ce dernier sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le handler d’événements pour l’instance Project Web App à l’aide de la page Project Server Paramètres de l’Paramètres d’application générale de l’Administration centrale de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9de0c-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="9de0c-130">**Configurer un ordinateur de développement.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="9de0c-131">Vous accédez généralement à l’interface PSI via un réseau.</span><span class="sxs-lookup"><span data-stu-id="9de0c-131">You usually access the PSI through a network.</span></span> <span data-ttu-id="9de0c-132">Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf en cas de remarque.</span><span class="sxs-lookup"><span data-stu-id="9de0c-132">The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="9de0c-133">**Installez la version correcte de Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="9de0c-134">Sauf remarque, les exemples de code sont écrits dans Visual C#.</span><span class="sxs-lookup"><span data-stu-id="9de0c-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="9de0c-135">Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="9de0c-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="9de0c-136">Assurez-vous que le Service Pack le plus récent est installé.</span><span class="sxs-lookup"><span data-stu-id="9de0c-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="9de0c-137">**Copiez Project DLLs de serveur sur l’ordinateur de développement.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="9de0c-138">Copiez les assemblys suivants à partir de `[Program Files]\Microsoft Office Servers\15.0\Bin` l’ordinateur Project Server vers l’ordinateur de développement :</span><span class="sxs-lookup"><span data-stu-id="9de0c-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="9de0c-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="9de0c-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="9de0c-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="9de0c-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="9de0c-141">Pour plus d’informations sur la compilation et l’utilisation de l’assembly de proxy ProjectServerServices.dll pour les services web ASMX dans l’interface PSI, voir Utilisation d’un assembly de proxy PSI et des [descriptions IntelliSense données.](#pj15_PrerequisitesASMX_BuildingProxy)</span><span class="sxs-lookup"><span data-stu-id="9de0c-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="9de0c-142">**Installez les IntelliSense fichiers.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="9de0c-143">Pour utiliser des descriptions IntelliSense pour les classes et les membres dans les assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du SDK Project 2013 dans le même répertoire que les assemblys Project Server.</span><span class="sxs-lookup"><span data-stu-id="9de0c-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="9de0c-144">Par exemple, copiez le fichier Microsoft.Office.Project.Server.Library.xml dans le répertoire où votre application définira une référence à l’assembly Microsoft.Office.Project.Server.Library.dll.</span><span class="sxs-lookup"><span data-stu-id="9de0c-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="9de0c-145">IntelliSense descriptions des services web PSI nécessitent la création d’un assembly de proxy PSI à l’aide du script CompileASMXProxyAssembly.cmd dans le sous-dossier du téléchargement du `Documentation\IntelliSense\WSDL` SDK Project 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="9de0c-146">Le script crée l’assembly ProjectServerServices.dll proxy asmx.</span><span class="sxs-lookup"><span data-stu-id="9de0c-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="9de0c-147">Pour plus d’informations, voir le fichier [ReadMe_IntelliSense] dans le téléchargement du SDK.</span><span class="sxs-lookup"><span data-stu-id="9de0c-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="9de0c-148">Création de l’application et ajout d’une référence de service web</span><span class="sxs-lookup"><span data-stu-id="9de0c-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="9de0c-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span></span>

1. <span data-ttu-id="9de0c-150">**Créez une application console.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="9de0c-151">Lorsque vous créez une application console, dans la liste de la boîte de dialogue **Nouveau Project,** sélectionnez **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="9de0c-151">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**.</span></span> <span data-ttu-id="9de0c-152">Vous pouvez copier l’exemple de code PSI dans la nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="9de0c-152">You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="9de0c-153">**Ajoutez la référence requise pour ASMX.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="9de0c-154">Dans l’Explorateur de solutions, ajoutez une référence **à System.Web.Services** (voir figure 1).</span><span class="sxs-lookup"><span data-stu-id="9de0c-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="9de0c-155">**Figure 1. Ajout d’une référence dans Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="9de0c-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="9de0c-156">![Ajout d’une référence dans Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "ajout d’une référence dans Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="9de0c-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="9de0c-157">**Copiez le code**.</span><span class="sxs-lookup"><span data-stu-id="9de0c-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="9de0c-158">Copiez l’exemple de code complet dans le fichier Program.cs de l’application console.</span><span class="sxs-lookup"><span data-stu-id="9de0c-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="9de0c-159">**Définissez l’espace de noms pour l’exemple d’application.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="9de0c-160">Vous pouvez modifier l’espace de noms répertorié en haut de l’exemple en espace de noms par défaut de l’application ou modifier l’espace de noms d’application par défaut pour qu’il corresponde à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-160">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample.</span></span> <span data-ttu-id="9de0c-161">Vous pouvez modifier l’espace de noms d’application par défaut en modifiant les propriétés de l’application.</span><span class="sxs-lookup"><span data-stu-id="9de0c-161">You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="9de0c-162">Par exemple, l’exemple de code [de QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) possède l’espace de noms **Microsoft.SDK.Project. Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="9de0c-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="9de0c-163">Si le nom du projet Visual Studio est **RenameProject,** copiez l’espace de noms à  partir du fichier Program.cs, puis ouvrez le volet Propriétés du projet (dans le menu **Project,** choisissez **RenameProject Properties**).</span><span class="sxs-lookup"><span data-stu-id="9de0c-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="9de0c-164">Sous **l’onglet Application,** copiez l’espace de noms dans la **zone de texte Espace de noms** par défaut.</span><span class="sxs-lookup"><span data-stu-id="9de0c-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="9de0c-165">**Définissez les références web.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="9de0c-166">La plupart des exemples nécessitent une référence à un ou plusieurs des services web PSI.</span><span class="sxs-lookup"><span data-stu-id="9de0c-166">Most examples require a reference to one or more of the PSI web services.</span></span> <span data-ttu-id="9de0c-167">Ceux-ci sont répertoriés dans l’exemple lui-même ou dans les commentaires qui précèdent l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-167">These are listed in the sample itself or in comments that precede the sample.</span></span> <span data-ttu-id="9de0c-168">Pour obtenir l’espace de noms correct des références web, assurez-vous que vous définissez d’abord l’espace de noms d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="9de0c-168">To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="9de0c-169">Il existe trois façons d’ajouter une référence de service web ASMX pour l’interface PSI :</span><span class="sxs-lookup"><span data-stu-id="9de0c-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="9de0c-170">Créez un assembly de proxy PSI ProjectServerServices.dll, puis définissez une référence à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9de0c-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="9de0c-171">Pour obtenir IntelliSense, il s’agit de la façon recommandée d’ajouter une référence PSI.</span><span class="sxs-lookup"><span data-stu-id="9de0c-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="9de0c-172">Voir [l’utilisation d’un assembly de proxy PSI et IntelliSense descriptions.](#pj15_PrerequisitesASMX_BuildingProxy)</span><span class="sxs-lookup"><span data-stu-id="9de0c-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="9de0c-173">Ajoutez un fichier proxy à partir de la wsdl.exe à la solution Visual Studio’accès.</span><span class="sxs-lookup"><span data-stu-id="9de0c-173">Add a proxy file from the wsdl.exe output to the Visual Studio solution.</span></span> <span data-ttu-id="9de0c-174">Voir [Ajout d’un fichier proxy PSI.](#pj15_PrerequisitesASMX_AddingProxyFile)</span><span class="sxs-lookup"><span data-stu-id="9de0c-174">See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="9de0c-175">Ajoutez une référence de service web à l’aide Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9de0c-175">Add a web service reference by using Visual Studio.</span></span> <span data-ttu-id="9de0c-176">Voir [Ajout d’une référence de service web.](#pj15_PrerequisitesASMX_AddingServiceReference)</span><span class="sxs-lookup"><span data-stu-id="9de0c-176">See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="9de0c-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="9de0c-178">Utilisation d’un assembly de proxy PSI et de descriptions IntelliSense données</span><span class="sxs-lookup"><span data-stu-id="9de0c-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="9de0c-179">Vous pouvez créer et utiliser l’assembly proxy ProjectServerServices.dll pour tous les services web ASMX dans l’interface PSI, à l’aide du script CompileASMXProxyAssembly.cmd dans le dossier du téléchargement du `Documentation\IntelliSense\WSDL` SDK Project 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="9de0c-180">Pour obtenir un lien vers le téléchargement, voir [Project 2013 pour les développeurs.](project-2013-developer-documentation.md)</span><span class="sxs-lookup"><span data-stu-id="9de0c-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9de0c-181">Lorsque vous extrayez les fichiers proxy sources du fichier Source.zip, les fichiers du dossier sont à jour à la date de publication du téléchargement du `Documentation\IntelliSense\WSDL\Source` SDK Project 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="9de0c-182">Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly.cmd sur l’ordinateur Project Server.</span><span class="sxs-lookup"><span data-stu-id="9de0c-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="9de0c-183">Les scripts du dossier  `Documentation\IntelliSense\WCF` ne fonctionnent pas pour les applications ASMX.</span><span class="sxs-lookup"><span data-stu-id="9de0c-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="9de0c-184">Le script GenWCFProxyAssembly.cmd appelle SvcUtil.exe, qui génère des fichiers de code source pour les services WCF.</span><span class="sxs-lookup"><span data-stu-id="9de0c-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="9de0c-185">Les fichiers proxy WCF incluent différents attributs, l’interface de canal et une classe cliente pour chaque service PSI.</span><span class="sxs-lookup"><span data-stu-id="9de0c-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="9de0c-186">Par exemple, le service de ressources WCF inclut l’interface **ResourceChannel,** l’interface **Resource** et la **classe ResourceClient.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="9de0c-187">Le site web de ressources ASMX inclut la classe **Resource** avec certaines propriétés différentes.</span><span class="sxs-lookup"><span data-stu-id="9de0c-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="9de0c-188">Voici le script GenASMXProxyAssembly.cmd qui génère des fichiers de sortie WSDL pour les services web PSI, puis compile l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9de0c-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

<span data-ttu-id="9de0c-189">Le script utilise le ClassList_asmx.txt, qui contient la liste des services web disponibles pour les développeurs tiers.</span><span class="sxs-lookup"><span data-stu-id="9de0c-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

<span data-ttu-id="9de0c-190">Les scripts créent un assembly nommé ProjectServerServices.dll.</span><span class="sxs-lookup"><span data-stu-id="9de0c-190">The scripts create an assembly named ProjectServerServices.dll.</span></span> <span data-ttu-id="9de0c-191">Évitez de le confondre avec ProjectServerServices.dll pour l’assembly WCF.</span><span class="sxs-lookup"><span data-stu-id="9de0c-191">Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly.</span></span> <span data-ttu-id="9de0c-192">Les noms d’assembly sont les mêmes, pour permettre l’utilisation de l’un ou l’autre assembly ProjectServerServices.xml IntelliSense fichier.</span><span class="sxs-lookup"><span data-stu-id="9de0c-192">The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="9de0c-193">L’espace de noms arbitraire créé par les scripts pour les services web ASMX et les services WCF est le même, de sorte que le fichier ProjectServerServices.xml IntelliSense fonctionne avec l’un ou l’autre assembly.</span><span class="sxs-lookup"><span data-stu-id="9de0c-193">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly.</span></span> <span data-ttu-id="9de0c-194">Par exemple, l’espace de noms du service ressource dans l’assembly de proxy WCF et dans l’assembly de proxy ASMX est **SvcResource**.</span><span class="sxs-lookup"><span data-stu-id="9de0c-194">For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**.</span></span> <span data-ttu-id="9de0c-195">Vous pouvez bien entendu modifier les noms des espaces de noms si vous vous assurez qu’ils correspondent dans l’assembly proxy et dans le ProjectServerServices.xml IntelliSense de noms.</span><span class="sxs-lookup"><span data-stu-id="9de0c-195">You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="9de0c-196">Si un exemple de code utilise un nom différent pour un espace de noms de service web PSI, par exemple **ProjectWebSvc**, pour que IntelliSense fonctionne, vous devez modifier l’exemple pour utiliser **SvcProject** afin que l’espace de noms corresponde à l’assembly de proxy.</span><span class="sxs-lookup"><span data-stu-id="9de0c-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="9de0c-197">L’un des avantages de l’assembly de proxy ASMX est qu’il inclut tous les espaces de noms du service web PSI ; vous n’avez pas besoin de créer plusieurs références Web.</span><span class="sxs-lookup"><span data-stu-id="9de0c-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="9de0c-198">Un autre avantage est que, si vous ajoutez le fichier ProjectServerServices.xml au même répertoire où vous définissez une référence à l’assembly proxy ProjectServerServices.dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI.</span><span class="sxs-lookup"><span data-stu-id="9de0c-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="9de0c-199">La figure 2 montre le IntelliSense texte de la **Project. Méthode QueueCreateProject.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="9de0c-200">Pour plus d’informations, voir le fichier [ReadMe_IntelliSense] dans le dossier IntelliSense du téléchargement du SDK Project 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="9de0c-201">**Figure 2. Utilisation IntelliSense pour une méthode dans le service web Project web**</span><span class="sxs-lookup"><span data-stu-id="9de0c-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="9de0c-202">![Utilisation d’Intellisense pour une méthode dans un service PSI]à l’aide d’Intellisense pour une méthode dans un service(media/pj15_PrerequisitesASMX_Intellisense.gif "PSI")</span><span class="sxs-lookup"><span data-stu-id="9de0c-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="9de0c-203">Les inconvénients de l’utilisation de l’assembly de proxy sont que la solution est plus grande et que vous devez distribuer et installer l’assembly de proxy avec la solution.</span><span class="sxs-lookup"><span data-stu-id="9de0c-203">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution.</span></span> <span data-ttu-id="9de0c-204">Vous devez également utiliser les mêmes espaces de noms que dans l’assembly proxy et les fichiers IntelliSense, sauf si vous modifiez le script et le fichier ProjectServerServices.xml IntelliSense pour utiliser des espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="9de0c-204">You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="9de0c-205">Ajout d’un fichier proxy PSI</span><span class="sxs-lookup"><span data-stu-id="9de0c-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="9de0c-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span></span>

<span data-ttu-id="9de0c-207">Le Project SDK 2013 inclut les fichiers sources générés par la commande Wsdl.exe pour l’assembly proxy.</span><span class="sxs-lookup"><span data-stu-id="9de0c-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="9de0c-208">Les fichiers sources se Source.zip dans  `Documentation\IntelliSense\ASMX` le sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="9de0c-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="9de0c-209">Au lieu de définir une référence à l’assembly proxy, vous pouvez ajouter un ou plusieurs des fichiers sources à une solution Visual Studio de proxy.</span><span class="sxs-lookup"><span data-stu-id="9de0c-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="9de0c-210">Par exemple, après l’exécution du script GenASMXProxyAssembly.cmd, ajoutez le wsdl. Project.cs à la solution.</span><span class="sxs-lookup"><span data-stu-id="9de0c-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="9de0c-211">Au lieu d’exécuter le script, vous pouvez exécuter les commandes suivantes pour générer un fichier source unique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="9de0c-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="9de0c-212">Pour définir un **objet Project** en tant que variable de classe nommée **projet,** utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="9de0c-212">To define a **Project** object as a class variable named **project**, use the following code.</span></span> <span data-ttu-id="9de0c-213">La **méthode AddContextInfo** ajoute les  informations de contexte à l’objet de projet pour Windows’authentification basée sur les formulaires et l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="9de0c-213">The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> <span data-ttu-id="9de0c-214">Que vous utilisez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcProject,** vous utiliseriez le même code pour créer un **objet de** projet.</span><span class="sxs-lookup"><span data-stu-id="9de0c-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="9de0c-215">Ajout d’une référence de service web</span><span class="sxs-lookup"><span data-stu-id="9de0c-215">Adding a web service reference</span></span>
<span data-ttu-id="9de0c-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span></span>

<span data-ttu-id="9de0c-217">Si vous n’utilisez pas l’assembly de proxy ASMX ou n’ajoutez pas de fichier de sortie WSDL, vous pouvez définir une ou plusieurs références web individuelles.</span><span class="sxs-lookup"><span data-stu-id="9de0c-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="9de0c-218">Les étapes suivantes montrent comment définir une référence web à l’aide Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="9de0c-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="9de0c-219">Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence de service.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="9de0c-220">Dans la **boîte de dialogue Ajouter une référence de service,** choisissez **Avancé.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="9de0c-221">Dans la **boîte de dialogue Référence Paramètres** service, choisissez Ajouter une référence **Web.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="9de0c-222">Dans la zone de texte **URL,** tapez, puis appuyez sur `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` **Entrée** ou choisissez **l’icône** Aller.</span><span class="sxs-lookup"><span data-stu-id="9de0c-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="9de0c-223">Si le protocole SSL (Secure Sockets Layer) est installé, vous devez utiliser le protocole HTTPS au lieu du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="9de0c-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="9de0c-224">Par exemple, utilisez l’URL suivante pour le service Project sur `https://MyServer/pwa` le site pour Project Web App :`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="9de0c-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="9de0c-225">Ou bien, ouvrez votre navigateur web et accédez à `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` .</span><span class="sxs-lookup"><span data-stu-id="9de0c-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="9de0c-226">Enregistrez le fichier dans un répertoire local, tel que `C:\Project\WebServices\ServiceName.wsdl` .</span><span class="sxs-lookup"><span data-stu-id="9de0c-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="9de0c-227">Dans la **boîte de dialogue Ajouter une référence Web,** pour **l’URL,** tapez le protocole de fichier et le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="9de0c-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="9de0c-228">Par exemple, tapez `file://C:\Project\WebServices\Project.wsdl` .</span><span class="sxs-lookup"><span data-stu-id="9de0c-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="9de0c-229">Une fois la référence résolue, tapez le nom de la référence dans la zone de texte **Nom de référence Web.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="9de0c-230">Les exemples de code de la documentation Project 2013 du développeur utilisent le nom de référence standard **arbitraire Svc _ServiceName_**.</span><span class="sxs-lookup"><span data-stu-id="9de0c-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="9de0c-231">Par exemple, le service web Project est **nommé SvcProject** (voir figure 3).</span><span class="sxs-lookup"><span data-stu-id="9de0c-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="9de0c-232">**Figure 3. Ajout d’une référence de service web ASMX**</span><span class="sxs-lookup"><span data-stu-id="9de0c-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="9de0c-233">![Ajout d’une référence de service web ASMX Ajout](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "d’une référence de service web ASMX")</span><span class="sxs-lookup"><span data-stu-id="9de0c-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="9de0c-234">Pour les composants d’application qui doivent s’exécuter sur l’ordinateur Project Server, utiliser l’emprunt d’identité ou avoir des autorisations élevées, utilisez une référence de service WCF au lieu d’une référence web ASMX.</span><span class="sxs-lookup"><span data-stu-id="9de0c-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="9de0c-235">Pour plus d’informations, [voir Conditions préalables pour les exemples](prerequisites-for-wcf-based-code-samples-in-project.md)de code basés sur WCF dans Project .</span><span class="sxs-lookup"><span data-stu-id="9de0c-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="9de0c-236">Définition d’autres références</span><span class="sxs-lookup"><span data-stu-id="9de0c-236">Setting other references</span></span>
<span data-ttu-id="9de0c-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span></span>

<span data-ttu-id="9de0c-238">Project Les applications serveur utilisent souvent d’autres services, tels que SharePoint services web Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="9de0c-239">Si d’autres services sont requis, ils sont indiqués dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="9de0c-240">Les références locales pour l’exemple de code sont répertoriées à l’aide d’instructions en haut de l’exemple : </span><span class="sxs-lookup"><span data-stu-id="9de0c-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="9de0c-241">Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="9de0c-242">**Sélectionnez** Parcourir, puis accédez à l’emplacement où vous avez stocké les DLL du serveur Project que vous avez copiées précédemment.</span><span class="sxs-lookup"><span data-stu-id="9de0c-242">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously.</span></span> <span data-ttu-id="9de0c-243">Choisissez les DLL dont vous avez besoin, puis **choisissez OK.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-243">Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9de0c-244">Assurez-vous que les versions d’assembly sur votre ordinateur de développement correspondent exactement à celles de l’ordinateur Project Server cible.</span><span class="sxs-lookup"><span data-stu-id="9de0c-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="9de0c-245">Utilisation de l’authentification multiple</span><span class="sxs-lookup"><span data-stu-id="9de0c-245">Using multiple authentication</span></span>
<span data-ttu-id="9de0c-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span></span>

<span data-ttu-id="9de0c-247">L’authentification des utilisateurs Project Server locaux, que ce soit par l’authentification Windows ou l’authentification par formulaires, est effectuée par le biais du traitement des revendications dans SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9de0c-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="9de0c-248">L’authentification multiple signifie que l’application web sur laquelle Project Web App est mise en service prend en charge l Windows’authentification basée sur les formulaires et l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="9de0c-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="9de0c-249">Si tel est le cas, un appel à un service web ASMX qui utilise l’authentification Windows échouera avec l’erreur suivante, car le processus de revendications ne peut pas déterminer le type d’utilisateur à authentifier :</span><span class="sxs-lookup"><span data-stu-id="9de0c-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="9de0c-250">Pour résoudre le problème d’ASMX, tous les appels aux méthodes PSI doivent être vers une classe dérivée définie pour chaque service web PSI.</span><span class="sxs-lookup"><span data-stu-id="9de0c-250">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service.</span></span> <span data-ttu-id="9de0c-251">La classe dérivée doit également utiliser la classe **SvcLoginWindows.LoginWindows** pour obtenir un cookie pour la classe de service PSI dérivée.</span><span class="sxs-lookup"><span data-stu-id="9de0c-251">The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class.</span></span> <span data-ttu-id="9de0c-252">Dans l’exemple suivant, la **classe ProjectDerived** dérive de **la classe SvcProject.Project.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-252">In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class.</span></span> <span data-ttu-id="9de0c-253">La classe dérivée ajoute la **propriété EnforceWindowsAuth** et remplace l’en-tête de requête web pour chaque appel à une méthode dans la **classe Project.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-253">The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class.</span></span> <span data-ttu-id="9de0c-254">Si la **propriété EnforceWindowsAuth** est **true,** la **méthode GetWebRequest** ajoute un en-tête qui désactive l’authentification par formulaires.</span><span class="sxs-lookup"><span data-stu-id="9de0c-254">If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication.</span></span> <span data-ttu-id="9de0c-255">Si **EnforceWindowsAuth est** **faux,** l’authentification par formulaires peut continuer.</span><span class="sxs-lookup"><span data-stu-id="9de0c-255">If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="9de0c-256">Pour utiliser l’exemple **de ASMXLogon_MultiAuth** suivant, créez une application console, suivez les étapes de Création de l’application et ajout d’une référence de [service web,](#pj15_PrerequisitesASMX_Configure)puis ajoutez le wsdl. Fichier proxy LoginWindows.cs et wsdl. Project.cs proxy.</span><span class="sxs-lookup"><span data-stu-id="9de0c-256">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file.</span></span> <span data-ttu-id="9de0c-257">La **méthode Main** crée l’instance de **projet** de la **classe ProjectDerived.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-257">The **Main** method creates the **project** instance of the **ProjectDerived** class.</span></span> <span data-ttu-id="9de0c-258">L’exemple doit utiliser la classe **dérivée LoginWindowsDerived** pour obtenir un objet **CookieContainer** pour le **projet. Propriété CookieContainer,** qui distingue l’authentification par formulaires de l’Windows’authentification par formulaire.</span><span class="sxs-lookup"><span data-stu-id="9de0c-258">The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication.</span></span> <span data-ttu-id="9de0c-259">**L’objet** projet peut ensuite être utilisé pour appeler n’importe quelle méthode de la **classe SvcProject.Project.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-259">The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9de0c-260">Le service **LoginWindows est** requis uniquement pour les applications ASMX dans un environnement d’authentification multiple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-260">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment.</span></span> <span data-ttu-id="9de0c-261">Dans **l ASMXLogon_MultiAuth** exemple, la **méthode GetLogonCookie** obtient un cookie pour l’objet **loginWindows.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-261">In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object.</span></span> <span data-ttu-id="9de0c-262">**Projet. La propriété CookieContainer** est définie sur la **valeur loginWindows.CookieContainer.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-262">The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

<span data-ttu-id="9de0c-263">L’utilisation de la classe **LoginWindows** dérivée et la réalisation d’appels PSI avec un en-tête de demande web qui désactive l’authentification par formulaires sont requises pour les applications qui s’exécutent dans un environnement d’authentification multiple.</span><span class="sxs-lookup"><span data-stu-id="9de0c-263">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment.</span></span> <span data-ttu-id="9de0c-264">Si Project server utilise uniquement l’authentification basée sur les revendications, il n’est pas nécessaire de dériver une classe qui ajoute un en-tête de requête web.</span><span class="sxs-lookup"><span data-stu-id="9de0c-264">If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header.</span></span> <span data-ttu-id="9de0c-265">L’exemple précédent s’exécute dans les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="9de0c-265">The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="9de0c-266">Le correctif d’une application WCF est différent.</span><span class="sxs-lookup"><span data-stu-id="9de0c-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="9de0c-267">Pour plus d’informations, voir la section Utilisation de *l’authentification* multiple dans Conditions préalables pour les exemples de code basés sur [WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="9de0c-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="9de0c-268">Modification des valeurs des constantes génériques</span><span class="sxs-lookup"><span data-stu-id="9de0c-268">Changing the values of generic constants</span></span>
<span data-ttu-id="9de0c-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span></span>

<span data-ttu-id="9de0c-270">La plupart des exemples ont une ou plusieurs variables que vous devez mettre à jour pour que l’exemple fonctionne correctement dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="9de0c-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="9de0c-271">Dans l’exemple suivant, si SSL est installé, utilisez le protocole HTTPS au lieu du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="9de0c-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="9de0c-272">Remplacez  _ServerName_ par le nom du serveur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="9de0c-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="9de0c-273">Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, tel que PWA.</span><span class="sxs-lookup"><span data-stu-id="9de0c-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="9de0c-274">Toutes les autres variables que vous devez modifier ou d’autres conditions préalables sont notées en haut de l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="9de0c-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="9de0c-275">Vérification des résultats</span><span class="sxs-lookup"><span data-stu-id="9de0c-275">Verifying the results</span></span>
<span data-ttu-id="9de0c-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span></span>

<span data-ttu-id="9de0c-277">L’obtention et l’interprétation des résultats à partir d’un exemple de code ne sont pas toujours simples.</span><span class="sxs-lookup"><span data-stu-id="9de0c-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="9de0c-278">Par exemple, si vous créez un projet, vous devez le publier pour qu’il puisse apparaître sur la page centre Project dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="9de0c-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="9de0c-279">Vous pouvez vérifier les résultats des exemples de code de plusieurs manières, par exemple :</span><span class="sxs-lookup"><span data-stu-id="9de0c-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="9de0c-280">Utilisez le client Project Professionnel 2013 pour ouvrir le projet à partir de l’ordinateur Project Server et afficher les éléments que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="9de0c-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="9de0c-281">Afficher les projets publiés sur la page Project centre de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="9de0c-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="9de0c-282">Affichez le journal de file d’attente Project Web App.</span><span class="sxs-lookup"><span data-stu-id="9de0c-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="9de0c-283">Ouvrez la page Paramètres serveur (sélectionnez l’icône **Paramètres** dans le  coin supérieur droit), puis choisissez Mes travaux en file d’attente sous la section **Paramètres** personnel ( `https://ServerName/ProjectServerName/MyJobs.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="9de0c-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="9de0c-284">Dans la **liste de** listes de listes listes, vous pouvez trier en fonction de l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="9de0c-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="9de0c-285">L’état par défaut **est En cours et Travaux en échec de la semaine dernière.**</span><span class="sxs-lookup"><span data-stu-id="9de0c-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="9de0c-286">Utilisez la page Serveur Paramètres dans Project Web App ( ) pour gérer tous les travaux en file d’attente et supprimer ou forcer l’enregistrement des objets `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9de0c-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="9de0c-287">Vous devez avoir des autorisations administratives pour accéder à ces liens sur la page Paramètres serveur.</span><span class="sxs-lookup"><span data-stu-id="9de0c-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="9de0c-288">Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table dans la base de données Project données.</span><span class="sxs-lookup"><span data-stu-id="9de0c-288">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database.</span></span> <span data-ttu-id="9de0c-289">Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes de la pub. MSP_WORKFLOW_STAGE_PDPS pour afficher des informations sur les pages de détails de projet (PDP) dans les étapes du flux de travail.</span><span class="sxs-lookup"><span data-stu-id="9de0c-289">For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a><span data-ttu-id="9de0c-290">Nettoyage</span><span class="sxs-lookup"><span data-stu-id="9de0c-290">Cleaning up</span></span>
<span data-ttu-id="9de0c-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span></span>

<span data-ttu-id="9de0c-292">Après avoir testé certains exemples de code, certains objets et paramètres d’entreprise doivent être supprimés ou réinitialisés.</span><span class="sxs-lookup"><span data-stu-id="9de0c-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="9de0c-293">Vous pouvez utiliser la page Serveur Paramètres dans Project Web App pour gérer les données d’entreprise ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="9de0c-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="9de0c-294">Les liens de la page Paramètres serveur vous permettent de supprimer les anciens éléments, de forcer l’enregistrement des projets, de gérer la file d’attente des travaux pour tous les utilisateurs et d’effectuer d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9de0c-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="9de0c-295">Voici quelques-uns des liens sur la page Serveur Paramètres que vous pouvez utiliser pour des activités de nettoyage classiques après l’exécution d’exemples de code :</span><span class="sxs-lookup"><span data-stu-id="9de0c-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="9de0c-296">**Champs personnalisés d’entreprise et tables de choix**</span><span class="sxs-lookup"><span data-stu-id="9de0c-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="9de0c-297">**Gérer les travaux en file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9de0c-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="9de0c-298">**Supprimer des objets d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="9de0c-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="9de0c-299">**Forcer l’Enterprise objets**</span><span class="sxs-lookup"><span data-stu-id="9de0c-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="9de0c-300">**Types de projets d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="9de0c-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="9de0c-301">**Phases du flux de travail**</span><span class="sxs-lookup"><span data-stu-id="9de0c-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="9de0c-302">**Étapes du flux de travail**</span><span class="sxs-lookup"><span data-stu-id="9de0c-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="9de0c-303">**Pages de détails de projet**</span><span class="sxs-lookup"><span data-stu-id="9de0c-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="9de0c-304">**Périodes de rapports de temps**</span><span class="sxs-lookup"><span data-stu-id="9de0c-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="9de0c-305">**Paramètres et valeurs par défaut de la feuille de temps**</span><span class="sxs-lookup"><span data-stu-id="9de0c-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="9de0c-306">**Classifications des lignes**</span><span class="sxs-lookup"><span data-stu-id="9de0c-306">**Line Classifications**</span></span>
    
<span data-ttu-id="9de0c-307">Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance Project Web App, plutôt que par une page Project Web App Server Paramètres spécifique.</span><span class="sxs-lookup"><span data-stu-id="9de0c-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="9de0c-308">In the SharePoint Central Administration application, choose **General Application Paramètres,** choose **Manage** under Project **Server Paramètres**, and then choose the Project Web App instance in the drop-down list on the Server Paramètres page.</span><span class="sxs-lookup"><span data-stu-id="9de0c-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="9de0c-309">Par exemple, sélectionnez **Les handlers** d’événements côté serveur pour ajouter ou supprimer des handlers d’événements pour l’instance Project Web App sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9de0c-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9de0c-310">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9de0c-310">See also</span></span>
<span data-ttu-id="9de0c-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="9de0c-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span></span>

- [<span data-ttu-id="9de0c-312">Conditions préalables pour les exemples de code basés sur WCF</span><span class="sxs-lookup"><span data-stu-id="9de0c-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="9de0c-313">Utiliser l’emprunt d’identité avec WCF</span><span class="sxs-lookup"><span data-stu-id="9de0c-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="9de0c-314">Vue d’ensemble de la référence Project PSI</span><span class="sxs-lookup"><span data-stu-id="9de0c-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="9de0c-315">Centre de développement SharePoint</span><span class="sxs-lookup"><span data-stu-id="9de0c-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

