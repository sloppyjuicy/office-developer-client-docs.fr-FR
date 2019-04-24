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
- exemples de code, Project Server, Project Server, programmation, PSI, compiler des exemples de code, PSI, programmation
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code ASMX qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357079"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="aaf42-104">Conditions préalables pour les exemples de code basés sur ASMX</span><span class="sxs-lookup"><span data-stu-id="aaf42-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="aaf42-105">Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code ASMX qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).</span><span class="sxs-lookup"><span data-stu-id="aaf42-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="aaf42-106">De nombreux exemples de code inclus dans la [bibliothèque de classes de Project Server 2013 et la référence de service Web](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été créés à l'origine pour le kit de développement logiciel (SDK) Office Project 2007, et utilisent un format standard pour les services Web ASMX.</span><span class="sxs-lookup"><span data-stu-id="aaf42-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="aaf42-107">Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu'unité complète.</span><span class="sxs-lookup"><span data-stu-id="aaf42-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="aaf42-108">Les exceptions sont indiquées dans l'exemple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="aaf42-109">Les nouveaux exemples PSI dans le kit de développement logiciel (SDK) Project 2013 sont conformes à un format qui utilise des services Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="aaf42-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="aaf42-110">Les exemples basés sur ASMX peuvent également être adaptés pour utiliser les services WCF.</span><span class="sxs-lookup"><span data-stu-id="aaf42-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="aaf42-111">Cet article explique comment utiliser les exemples avec les services Web ASMX.</span><span class="sxs-lookup"><span data-stu-id="aaf42-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="aaf42-112">Pour plus d'informations sur l'utilisation des exemples avec les services WCF, reportez-vous à la section [conditions préalables pour les exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="aaf42-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="aaf42-113">L’interface de service web ASMX de la PSI déconseillé dans Project Server 2013, mais est toujours prise en charge.</span><span class="sxs-lookup"><span data-stu-id="aaf42-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="aaf42-114">Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, les nouvelles applications doivent être développées avec le CSOM.</span><span class="sxs-lookup"><span data-stu-id="aaf42-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="aaf42-115">Le CSOM permet aux applications de fonctionner avec Project Online ou une installation locale de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="aaf42-116">Dans le cas contraire, si votre application utilise la PSI, elle doit utiliser l'interface WCF, qui est la technologie recommandée pour les communications réseau.</span><span class="sxs-lookup"><span data-stu-id="aaf42-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="aaf42-117">Les applications qui utilisent l'interface ASMX ou l'interface WCF peuvent fonctionner uniquement pour les installations locales de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="aaf42-118">Pour plus d'informations sur les CSOM, consultez la rubrique [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-Side Object Model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="aaf42-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="aaf42-119">Avant d'exécuter les exemples de code, vous devez configurer l'environnement de développement, configurer l'application et modifier les valeurs des constantes génériques en fonction de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="aaf42-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="aaf42-120">Configuration de l'environnement de développement</span><span class="sxs-lookup"><span data-stu-id="aaf42-120">Setting up the development environment</span></span>
<span data-ttu-id="aaf42-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-121"></span></span>

1. <span data-ttu-id="aaf42-122">**Configurez un système Project Server de test**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="aaf42-123">Utilisez un système Project Server de test chaque fois que vous effectuez des tests ou des développements.</span><span class="sxs-lookup"><span data-stu-id="aaf42-123">Use a test Project Server system whenever you are developing or testing.</span></span> <span data-ttu-id="aaf42-124">Même si votre code fonctionne parfaitement, les dépendances entre projets, la création de rapports ou d'autres facteurs environnementaux peuvent avoir des conséquences inattendues.</span><span class="sxs-lookup"><span data-stu-id="aaf42-124">Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="aaf42-125">Assurez-vous que vous êtes un utilisateur valide sur le serveur et vérifiez que vous disposez des autorisations suffisantes pour les appels PSI que votre application utilise.</span><span class="sxs-lookup"><span data-stu-id="aaf42-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="aaf42-126">La rubrique de référence pour chaque méthode PSI inclut une table d'autorisations de Project Server.</span><span class="sxs-lookup"><span data-stu-id="aaf42-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="aaf42-127">Par exemple, la méthode [Project. QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l'autorisation globale **NewProject** et l'autorisation **SaveProjectTemplate** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="aaf42-128">Dans certains cas, vous devrez peut-être effectuer un débogage à distance sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="aaf42-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="aaf42-129">Vous devrez peut-être également configurer un gestionnaire d'événements en installant un assembly de gestionnaire d'événements sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le gestionnaire d'événements pour l'instance de Project Web App à l'aide de la page Paramètres de Project Server dans le grand Paramètres d'application de l'administration centrale de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="aaf42-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="aaf42-130">**ConFigurez un ordinateur de développement.**</span><span class="sxs-lookup"><span data-stu-id="aaf42-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="aaf42-131">En règle générale, vous accédez à l'interface PSI via un réseau.</span><span class="sxs-lookup"><span data-stu-id="aaf42-131">You usually access the PSI through a network.</span></span> <span data-ttu-id="aaf42-132">Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="aaf42-132">The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="aaf42-133">**Installez la version appropriée de Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="aaf42-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="aaf42-134">Sauf indication contraire, les exemples de code sont écrits en Visual C#.</span><span class="sxs-lookup"><span data-stu-id="aaf42-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="aaf42-135">Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="aaf42-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="aaf42-136">Assurez-vous que le Service Pack le plus récent est installé.</span><span class="sxs-lookup"><span data-stu-id="aaf42-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="aaf42-137">**Copiez les dll Project Server sur l'ordinateur de développement.**</span><span class="sxs-lookup"><span data-stu-id="aaf42-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="aaf42-138">Copiez les assemblys suivants `[Program Files]\Microsoft Office Servers\15.0\Bin` de sur l'ordinateur Project Server vers l'ordinateur de développement:</span><span class="sxs-lookup"><span data-stu-id="aaf42-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="aaf42-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="aaf42-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="aaf42-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="aaf42-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="aaf42-141">Pour plus d'informations sur la compilation et l'utilisation de l'assembly de proxy ProjectServerServices. dll pour les services Web ASMX dans le PSI, voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="aaf42-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="aaf42-142">**Installez les fichiers IntelliSense.**</span><span class="sxs-lookup"><span data-stu-id="aaf42-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="aaf42-143">Pour utiliser les descriptions IntelliSense pour les classes et les membres des assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du kit de développement logiciel (SDK) Project 2013 dans le même répertoire où se trouvent les assemblys Project Server.</span><span class="sxs-lookup"><span data-stu-id="aaf42-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="aaf42-144">Par exemple, copiez le fichier Microsoft. Office. Project. Server. Library. xml dans le répertoire dans lequel votre application définira une référence à l'assembly Microsoft. Office. Project. Server. Library. dll.</span><span class="sxs-lookup"><span data-stu-id="aaf42-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="aaf42-145">Pour les services Web PSI, les descriptions IntelliSense vous obligent à créer un assembly de proxy PSI à l'aide du `Documentation\IntelliSense\WSDL` script CompileASMXProxyAssembly. cmd dans le sous-répertoire du téléchargement du kit de développement logiciel (SDK) de Project 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="aaf42-146">Le script crée l'assembly de proxy ProjectServerServices. dll basé sur ASMX.</span><span class="sxs-lookup"><span data-stu-id="aaf42-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="aaf42-147">Pour plus d'informations, consultez le fichier [ReadMe_IntelliSense] dans le téléchargement du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="aaf42-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="aaf42-148">Création de l'application et ajout d'une référence de service Web</span><span class="sxs-lookup"><span data-stu-id="aaf42-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="aaf42-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-149"></span></span>

1. <span data-ttu-id="aaf42-150">**Créez une application console**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="aaf42-151">Lorsque vous créez une application console, dans la liste déroulante de la boîte de dialogue **nouveau projet** , sélectionnez **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-151">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**.</span></span> <span data-ttu-id="aaf42-152">Vous pouvez copier l'exemple de code PSI dans la nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="aaf42-152">You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="aaf42-153">**Ajoutez la référence requise pour ASMX.**</span><span class="sxs-lookup"><span data-stu-id="aaf42-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="aaf42-154">Dans l'Explorateur de solutions, ajoutez une référence à **System. Web. services** (voir figure 1).</span><span class="sxs-lookup"><span data-stu-id="aaf42-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="aaf42-155">**Figure 1. Ajout d'une référence dans Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="aaf42-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="aaf42-156">![Ajout d'une référence dans Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Ajout d'une référence dans Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="aaf42-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="aaf42-157">**Copiez le code**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="aaf42-158">Copiez l'exemple de code complet dans le fichier Program.cs de l'application console.</span><span class="sxs-lookup"><span data-stu-id="aaf42-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="aaf42-159">**Définissez l'espace de noms pour l'exemple d'application**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="aaf42-160">Vous pouvez modifier l'espace de noms mentionné en haut de l'exemple pour l'espace de noms de l'application par défaut ou modifier l'espace de noms de l'application par défaut pour qu'il corresponde à l'exemple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-160">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample.</span></span> <span data-ttu-id="aaf42-161">Vous pouvez modifier l'espace de noms de l'application par défaut en modifiant les propriétés de l'application.</span><span class="sxs-lookup"><span data-stu-id="aaf42-161">You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="aaf42-162">Par exemple, l'exemple de code pour [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) a l'espace de noms **Microsoft. Sdk. Project. Samples. RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="aaf42-163">Si le nom du projet Visual Studio est **RenameProject**, copiez l'espace de noms à partir du fichier Program.cs, puis ouvrez le volet des **Propriétés** du projet (dans le menu **projet** , choisissez **Propriétés RenameProject**).</span><span class="sxs-lookup"><span data-stu-id="aaf42-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="aaf42-164">Dans l'onglet **application** , copiez l'espace de noms dans la zone de texte **espace de noms par défaut** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="aaf42-165">**Définissez les références Web**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="aaf42-166">La plupart des exemples nécessitent une référence à un ou plusieurs des services Web PSI.</span><span class="sxs-lookup"><span data-stu-id="aaf42-166">Most examples require a reference to one or more of the PSI web services.</span></span> <span data-ttu-id="aaf42-167">Celles-ci sont répertoriées dans l'exemple lui-même ou dans les commentaires qui précèdent l'exemple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-167">These are listed in the sample itself or in comments that precede the sample.</span></span> <span data-ttu-id="aaf42-168">Pour obtenir l'espace de noms approprié des références Web, vérifiez que vous avez d'abord défini l'espace de noms de l'application par défaut.</span><span class="sxs-lookup"><span data-stu-id="aaf42-168">To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="aaf42-169">Il existe trois façons d'ajouter une référence de service Web ASMX pour la PSI:</span><span class="sxs-lookup"><span data-stu-id="aaf42-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="aaf42-170">Créez un assembly de proxy PSI nommé ProjectServerServices. dll, puis définissez une référence à l'assembly.</span><span class="sxs-lookup"><span data-stu-id="aaf42-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="aaf42-171">Pour obtenir IntelliSense, il est recommandé d'ajouter une référence PSI.</span><span class="sxs-lookup"><span data-stu-id="aaf42-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="aaf42-172">Voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="aaf42-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="aaf42-173">Ajoutez un fichier proxy à partir de la sortie WSDL. exe vers la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aaf42-173">Add a proxy file from the wsdl.exe output to the Visual Studio solution.</span></span> <span data-ttu-id="aaf42-174">Consultez [la rubrique Ajout d'un fichier proxy PSI](#pj15_PrerequisitesASMX_AddingProxyFile).</span><span class="sxs-lookup"><span data-stu-id="aaf42-174">See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="aaf42-175">Ajoutez une référence de service Web à l'aide de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aaf42-175">Add a web service reference by using Visual Studio.</span></span> <span data-ttu-id="aaf42-176">Consultez [la rubrique Ajout d'une référence de service Web](#pj15_PrerequisitesASMX_AddingServiceReference).</span><span class="sxs-lookup"><span data-stu-id="aaf42-176">See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="aaf42-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-177"></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="aaf42-178">Utilisation d'un assembly de proxy PSI et descriptions IntelliSense</span><span class="sxs-lookup"><span data-stu-id="aaf42-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="aaf42-179">Vous pouvez créer et utiliser l'assembly de proxy ProjectServerServices. dll pour tous les services Web ASMX dans le PSI, en utilisant le script CompileASMXProxyAssembly. cmd dans `Documentation\IntelliSense\WSDL` le dossier du téléchargement du kit de développement logiciel (SDK) de Project 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="aaf42-180">Pour obtenir un lien vers le téléchargement, reportez-vous à la [documentation du développeur Project 2013](project-2013-developer-documentation.md).</span><span class="sxs-lookup"><span data-stu-id="aaf42-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="aaf42-181">Lorsque vous extrayez les fichiers sources proxy à partir du fichier. zip source, les `Documentation\IntelliSense\WSDL\Source` fichiers du dossier sont actualisés à la date de publication du téléchargement du kit de développement logiciel (SDK) Project 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="aaf42-182">Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly. cmd sur l'ordinateur Project Server.</span><span class="sxs-lookup"><span data-stu-id="aaf42-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="aaf42-183">Les scripts du `Documentation\IntelliSense\WCF` dossier ne fonctionnent pas pour les applications basées sur ASMX.</span><span class="sxs-lookup"><span data-stu-id="aaf42-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="aaf42-184">Le script GenWCFProxyAssembly. cmd appelle SvcUtil. exe, qui génère des fichiers de code source pour les services WCF.</span><span class="sxs-lookup"><span data-stu-id="aaf42-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="aaf42-185">Les fichiers de proxy WCF incluent différents attributs, l'interface de canal et une classe client pour chaque service PSI.</span><span class="sxs-lookup"><span data-stu-id="aaf42-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="aaf42-186">Par exemple, le service de ressources basées sur WCF inclut l'interface **ResourceChannel** , l'interface de **ressource** et la classe **ResourceClient** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="aaf42-187">Le site Web de ressource ASMX inclut la classe de **ressource** avec certaines propriétés.</span><span class="sxs-lookup"><span data-stu-id="aaf42-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="aaf42-188">Voici le script GenASMXProxyAssembly. cmd qui génère des fichiers de sortie WSDL pour les services Web PSI, puis compile l'assembly.</span><span class="sxs-lookup"><span data-stu-id="aaf42-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
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

<span data-ttu-id="aaf42-189">Le script utilise le fichier ClassList_asmx. txt, qui contient la liste des services Web disponibles pour les développeurs tiers.</span><span class="sxs-lookup"><span data-stu-id="aaf42-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
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

<span data-ttu-id="aaf42-190">Les scripts créent un assembly nommé ProjectServerServices. dll.</span><span class="sxs-lookup"><span data-stu-id="aaf42-190">The scripts create an assembly named ProjectServerServices.dll.</span></span> <span data-ttu-id="aaf42-191">Évitez de le confondre avec ProjectServerServices. dll pour l'assembly basé sur WCF.</span><span class="sxs-lookup"><span data-stu-id="aaf42-191">Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly.</span></span> <span data-ttu-id="aaf42-192">Les noms d'assembly sont les mêmes, pour permettre l'utilisation de l'assembly avec le fichier IntelliSense ProjectServerServices. Xml.</span><span class="sxs-lookup"><span data-stu-id="aaf42-192">The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="aaf42-193">L'espace de noms arbitraire créé par les scripts pour les services Web ASMX et les services WCF est le même, de sorte que le fichier ProjectServerServices. XML IntelliSense fonctionne avec l'un ou l'autre assembly.</span><span class="sxs-lookup"><span data-stu-id="aaf42-193">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly.</span></span> <span data-ttu-id="aaf42-194">Par exemple, l'espace de noms du service de ressources dans l'assembly de proxy basé sur WCF et dans l'assembly de proxy ASMX est **SvcResource**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-194">For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**.</span></span> <span data-ttu-id="aaf42-195">Vous pouvez bien sûr modifier les noms d'espace de noms — si vous vous assurez qu'ils correspondent dans l'assembly de proxy et dans le fichier ProjectServerServices. XML IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="aaf42-195">You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="aaf42-196">Si un exemple de code utilise un nom différent pour un espace de noms de service Web PSI, par exemple **ProjectWebSvc**, pour qu'IntelliSense fonctionne, vous devez modifier l'exemple afin qu'il utilise **SvcProject** afin que l'espace de noms corresponde à l'assembly de proxy.</span><span class="sxs-lookup"><span data-stu-id="aaf42-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="aaf42-197">L'un des avantages de l'utilisation de l'assembly de proxy basé sur ASMX est qu'il inclut tous les espaces de noms de service Web PSI; Il n'est pas nécessaire de créer plusieurs références Web.</span><span class="sxs-lookup"><span data-stu-id="aaf42-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="aaf42-198">Un autre avantage est que, si vous ajoutez le fichier ProjectServerServices. xml dans le même répertoire où vous avez défini une référence à l'assembly de proxy ProjectServerServices. dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI.</span><span class="sxs-lookup"><span data-stu-id="aaf42-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="aaf42-199">La figure 2 illustre le texte IntelliSense de la méthode **Project. QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="aaf42-200">Pour plus d'informations, consultez le fichier [ReadMe_IntelliSense] dans le dossier IntelliSense du téléchargement du kit de développement logiciel (SDK) de Project 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="aaf42-201">**Figure 2. Utilisation d'IntelliSense pour une méthode dans le service Web de projet**</span><span class="sxs-lookup"><span data-stu-id="aaf42-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="aaf42-202">![Utilisation d'IntelliSense pour une méthode dans un service PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Utilisation d'IntelliSense pour une méthode dans un service PSI")</span><span class="sxs-lookup"><span data-stu-id="aaf42-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="aaf42-203">Les inconvénients de l'utilisation de l'assembly de proxy sont les suivants: la solution est plus grande et vous devez distribuer et installer l'assembly de proxy avec la solution.</span><span class="sxs-lookup"><span data-stu-id="aaf42-203">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution.</span></span> <span data-ttu-id="aaf42-204">Vous devez également utiliser les mêmes espaces de noms que ceux qui se trouvent dans l'assembly de proxy et les fichiers IntelliSense, sauf si vous modifiez le fichier ProjectServerServices. xml et le script pour utiliser des espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="aaf42-204">You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="aaf42-205">Ajout d'un fichier proxy PSI</span><span class="sxs-lookup"><span data-stu-id="aaf42-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="aaf42-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-206"></span></span>

<span data-ttu-id="aaf42-207">Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut les fichiers sources générés par la commande WSDL. exe pour l'assembly de proxy.</span><span class="sxs-lookup"><span data-stu-id="aaf42-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="aaf42-208">Les fichiers sources se trouvent dans le fichier source. `Documentation\IntelliSense\ASMX` zip, dans le sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="aaf42-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="aaf42-209">Au lieu de définir une référence à l'assembly de proxy, vous pouvez ajouter un ou plusieurs fichiers sources à une solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aaf42-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="aaf42-210">Par exemple, après avoir exécuté le script GenASMXProxyAssembly. cmd, ajoutez le WSDL. Fichier Project.cs à la solution.</span><span class="sxs-lookup"><span data-stu-id="aaf42-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="aaf42-211">Au lieu d'exécuter le script, vous pouvez exécuter les commandes suivantes pour générer un fichier source unique, par exemple:</span><span class="sxs-lookup"><span data-stu-id="aaf42-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="aaf42-212">Pour définir un objet **Project** en tant que variable de classe nommée **Project**, utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="aaf42-212">To define a **Project** object as a class variable named **project**, use the following code.</span></span> <span data-ttu-id="aaf42-213">La méthode **AddContextInfo** ajoute les informations de contexte à l'objet **Project** pour l'authentification Windows et l'authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="aaf42-213">The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
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
> <span data-ttu-id="aaf42-214">Que vous utilisiez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcProject**, vous devez utiliser le même code pour créer un objet **Project** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="aaf42-215">Ajout d'une référence de service Web</span><span class="sxs-lookup"><span data-stu-id="aaf42-215">Adding a web service reference</span></span>
<span data-ttu-id="aaf42-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-216"></span></span>

<span data-ttu-id="aaf42-217">Si vous n'utilisez pas l'assembly de proxy basé sur ASMX ou si vous ajoutez un fichier de sortie WSDL, vous pouvez définir une ou plusieurs références Web individuelles.</span><span class="sxs-lookup"><span data-stu-id="aaf42-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="aaf42-218">Les étapes suivantes montrent comment définir une référence Web à l'aide de Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="aaf42-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="aaf42-219">Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence de service**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="aaf42-220">Dans la boîte de dialogue **Ajouter une référence de service** , sélectionnez **avancé**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="aaf42-221">Dans la boîte de dialogue **paramètres de référence de service** , sélectionnez Ajouter une **référence Web**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="aaf42-222">Dans la zone de texte **URL** , `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`tapez, puis appuyez sur **entrée** ou cliquez sur l'icône **OK** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="aaf42-223">Si le protocole SSL (Secure Sockets Layer) est installé, vous devez utiliser le protocole HTTPs au lieu du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="aaf42-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="aaf42-224">Par exemple, utilisez l'URL suivante pour le service Project sur le `https://MyServer/pwa` site pour Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="aaf42-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="aaf42-225">Ou ouvrez votre navigateur Web et accédez à `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span><span class="sxs-lookup"><span data-stu-id="aaf42-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="aaf42-226">Enregistrez le fichier dans un répertoire local, tel que `C:\Project\WebServices\ServiceName.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="aaf42-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="aaf42-227">Dans la boîte de dialogue **Ajouter une référence Web** , dans **URL**, tapez le protocole de fichier et le chemin d'accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="aaf42-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="aaf42-228">Par exemple, tapez `file://C:\Project\WebServices\Project.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="aaf42-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="aaf42-229">Une fois que la référence est résolue, tapez le nom de la référence dans la zone de texte nom de la **référence Web** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="aaf42-230">Les exemples de code dans la documentation du développeur Project 2013 utilisent le nom de référence standard arbitraire \*\* _ServiceName_\*\*.</span><span class="sxs-lookup"><span data-stu-id="aaf42-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="aaf42-231">Par exemple, le service Web de projet est nommé **SvcProject** (voir figure 3).</span><span class="sxs-lookup"><span data-stu-id="aaf42-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="aaf42-232">**Figure 3. Ajout d'une référence de service Web ASMX**</span><span class="sxs-lookup"><span data-stu-id="aaf42-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="aaf42-233">![Ajout d'une référence de service Web ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Ajout d'une référence de service Web ASMX")</span><span class="sxs-lookup"><span data-stu-id="aaf42-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="aaf42-234">Pour les composants d'application qui doivent s'exécuter sur l'ordinateur Project Server, utiliser l'emprunt d'identité ou avoir des autorisations élevées, utilisez une référence de service WCF au lieu d'une référence Web ASMX.</span><span class="sxs-lookup"><span data-stu-id="aaf42-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="aaf42-235">Pour plus d'informations, reportez-vous à la rubrique [conditions préalables pour les exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="aaf42-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="aaf42-236">Définition d'autres références</span><span class="sxs-lookup"><span data-stu-id="aaf42-236">Setting other references</span></span>
<span data-ttu-id="aaf42-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-237"></span></span>

<span data-ttu-id="aaf42-238">Les applications Project Server utilisent souvent d'autres services, tels que les services Web SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="aaf42-239">Si d'autres services sont requis, ils sont indiqués dans l'exemple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="aaf42-240">Les références locales de l'exemple de code sont répertoriées dans instructions **using** en haut de l'exemple:</span><span class="sxs-lookup"><span data-stu-id="aaf42-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="aaf42-241">Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="aaf42-242">Choisissez **Parcourir**, puis accédez à l'emplacement où vous avez stocké les dll Project Server que vous avez copiées précédemment.</span><span class="sxs-lookup"><span data-stu-id="aaf42-242">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously.</span></span> <span data-ttu-id="aaf42-243">Choisissez les dll dont vous avez besoin, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-243">Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="aaf42-244">Assurez-vous que les versions d'assembly de votre ordinateur de développement correspondent exactement à celles de l'ordinateur Project Server cible.</span><span class="sxs-lookup"><span data-stu-id="aaf42-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="aaf42-245">Utilisation de l'authentification multiple</span><span class="sxs-lookup"><span data-stu-id="aaf42-245">Using multiple authentication</span></span>
<span data-ttu-id="aaf42-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-246"></span></span>

<span data-ttu-id="aaf42-247">L'authentification des utilisateurs Project Server locaux, qu'il s'agisse de l'authentification Windows ou de l'authentification par formulaires, est réalisée via le traitement des revendications dans SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf42-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="aaf42-248">L'authentification multiple signifie que l'application Web sur laquelle est configuré Project Web App prend en charge l'authentification Windows et l'authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="aaf42-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="aaf42-249">Si c'est le cas, un appel à un service Web ASMX qui utilise l'authentification Windows échouera avec l'erreur suivante, car le processus de revendications ne peut pas déterminer le type d'utilisateur à authentifier:</span><span class="sxs-lookup"><span data-stu-id="aaf42-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="aaf42-250">Pour résoudre le problème pour ASMX, tous les appels aux méthodes PSI doivent être effectués sur une classe dérivée définie pour chaque service Web PSI.</span><span class="sxs-lookup"><span data-stu-id="aaf42-250">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service.</span></span> <span data-ttu-id="aaf42-251">La classe dérivée doit également utiliser la classe **SvcLoginWindows. serviceloginwindowsest** pour obtenir un cookie pour la classe de service PSI dérivée.</span><span class="sxs-lookup"><span data-stu-id="aaf42-251">The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class.</span></span> <span data-ttu-id="aaf42-252">Dans l'exemple suivant, la classe **ProjectDerived** dérive de la classe **SvcProject. Project** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-252">In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class.</span></span> <span data-ttu-id="aaf42-253">La classe dérivée ajoute la propriété **EnforceWindowsAuth** et remplace l'en-tête de requête Web pour chaque appel à une méthode dans la classe **Project** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-253">The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class.</span></span> <span data-ttu-id="aaf42-254">Si la propriété **EnforceWindowsAuth** a la **valeur true**, la méthode **GetWebRequest** ajoute un en-tête qui désactive l'authentification par formulaire.</span><span class="sxs-lookup"><span data-stu-id="aaf42-254">If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication.</span></span> <span data-ttu-id="aaf42-255">Si **EnforceWindowsAuth** a la **valeur false**, l'authentification par formulaire peut se poursuivre.</span><span class="sxs-lookup"><span data-stu-id="aaf42-255">If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="aaf42-256">Pour utiliser l'exemple **ASMXLogon_MultiAuth** suivant, créez une application console, suivez les étapes de [création de l'application et d'ajout d'une référence de service Web](#pj15_PrerequisitesASMX_Configure), puis ajoutez le WSDL. Fichier proxy LoginWindows.cs et WSDL. Fichier proxy Project.cs.</span><span class="sxs-lookup"><span data-stu-id="aaf42-256">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file.</span></span> <span data-ttu-id="aaf42-257">La méthode **main** crée l'instance de **projet** de la classe **ProjectDerived** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-257">The **Main** method creates the **project** instance of the **ProjectDerived** class.</span></span> <span data-ttu-id="aaf42-258">L'exemple doit utiliser la classe dérivée **LoginWindowsDerived** pour obtenir un objet **CookieContainer** pour le **projet. Propriété CookieContainer** , qui distingue l'authentification par formulaire de l'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="aaf42-258">The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication.</span></span> <span data-ttu-id="aaf42-259">L'objet **Project** peut ensuite être utilisé pour effectuer des appels à n'importe quelle méthode dans la classe **SvcProject. Project** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-259">The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aaf42-260">Le service **serviceloginwindowsest** est uniquement requis pour les applications asmx dans un environnement à plusieurs authentifications.</span><span class="sxs-lookup"><span data-stu-id="aaf42-260">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment.</span></span> <span data-ttu-id="aaf42-261">Dans l'exemple **ASMXLogon_MultiAuth** , la méthode **GetLogonCookie** obtient un cookie pour l'objet **serviceloginwindowsest** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-261">In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object.</span></span> <span data-ttu-id="aaf42-262">Le \*\*projet. \*\*La propriété CookieContainer est définie sur la valeur **Serviceloginwindowsest. CookieContainer** .</span><span class="sxs-lookup"><span data-stu-id="aaf42-262">The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
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

<span data-ttu-id="aaf42-263">L'utilisation de la classe **serviceloginwindowsest** dérivée et la création d'appels PSI avec un en-tête de requête Web qui désactive l'authentification par formulaires sont requises pour les applications qui s'exécutent dans un environnement à authentification multiple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-263">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment.</span></span> <span data-ttu-id="aaf42-264">Si Project Server utilise uniquement l'authentification basée sur les revendications, il n'est pas nécessaire de dériver une classe qui ajoute un en-tête de requête Web.</span><span class="sxs-lookup"><span data-stu-id="aaf42-264">If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header.</span></span> <span data-ttu-id="aaf42-265">L'exemple précédent s'exécute dans les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="aaf42-265">The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="aaf42-266">Le correctif pour une application basée sur WCF est différent.</span><span class="sxs-lookup"><span data-stu-id="aaf42-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="aaf42-267">Pour plus d'informations, reportez-vous à la section *utilisation de plusieurs authentifications* dans les [exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="aaf42-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="aaf42-268">Modification des valeurs des constantes génériques</span><span class="sxs-lookup"><span data-stu-id="aaf42-268">Changing the values of generic constants</span></span>
<span data-ttu-id="aaf42-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-269"></span></span>

<span data-ttu-id="aaf42-270">La plupart des exemples contiennent une ou plusieurs variables que vous devez mettre à jour pour que l'exemple fonctionne correctement dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="aaf42-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="aaf42-271">Dans l'exemple suivant, si SSL est installé, utilisez le protocole HTTPs au lieu du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="aaf42-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="aaf42-272">Remplacez _ServerName_ par le nom du serveur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="aaf42-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="aaf42-273">Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, par exemple, PWA.</span><span class="sxs-lookup"><span data-stu-id="aaf42-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="aaf42-274">Toutes les autres variables que vous devez modifier ou d'autres conditions préalables sont indiquées dans la partie supérieure de l'exemple de code.</span><span class="sxs-lookup"><span data-stu-id="aaf42-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="aaf42-275">Vérification des résultats</span><span class="sxs-lookup"><span data-stu-id="aaf42-275">Verifying the results</span></span>
<span data-ttu-id="aaf42-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-276"></span></span>

<span data-ttu-id="aaf42-277">L'obtention et l'interprétation de résultats à partir d'un exemple de code n'est pas toujours simple.</span><span class="sxs-lookup"><span data-stu-id="aaf42-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="aaf42-278">Par exemple, si vous créez un projet, vous devez publier le projet avant de pouvoir l'afficher sur la page Centre de projets dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="aaf42-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="aaf42-279">Vous pouvez vérifier les résultats de l'exemple de code de plusieurs façons, par exemple:</span><span class="sxs-lookup"><span data-stu-id="aaf42-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="aaf42-280">Utilisez le client Project Professional 2013 pour ouvrir le projet à partir de l'ordinateur Project Server et afficher les éléments de votre choix.</span><span class="sxs-lookup"><span data-stu-id="aaf42-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="aaf42-281">Affichez les projets publiés sur la page Centre de projets de Project `https://ServerName/ProjectServerName/projects.aspx`Web App ().</span><span class="sxs-lookup"><span data-stu-id="aaf42-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="aaf42-282">Affichez le journal de la file d'attente dans Project Web App.</span><span class="sxs-lookup"><span data-stu-id="aaf42-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="aaf42-283">Ouvrez la page Paramètres du serveur (cliquez sur l'icône **paramètres** dans le coin supérieur droit), puis choisissez **mes travaux en file d'attente** sous la section **paramètres personnels** ( `https://ServerName/ProjectServerName/MyJobs.aspx`).</span><span class="sxs-lookup"><span data-stu-id="aaf42-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="aaf42-284">Dans la liste déroulante **affichage** , vous pouvez trier en fonction de l'état du travail.</span><span class="sxs-lookup"><span data-stu-id="aaf42-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="aaf42-285">L'État par défaut est **en cours et échecs de travaux au cours de la semaine précédente**.</span><span class="sxs-lookup"><span data-stu-id="aaf42-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="aaf42-286">Utilisez la page Paramètres du serveur dans Project Web App `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`() pour gérer tous les travaux en file d'attente et supprimer ou forcer l'archivage des objets d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="aaf42-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="aaf42-287">Vous devez disposer d'autorisations d'administration pour accéder à ces liens sur la page Paramètres du serveur.</span><span class="sxs-lookup"><span data-stu-id="aaf42-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="aaf42-288">Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table dans la base de données Project.</span><span class="sxs-lookup"><span data-stu-id="aaf42-288">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database.</span></span> <span data-ttu-id="aaf42-289">Par exemple, utilisez la requête suivante pour sélectionner les premières 200 lignes du pub. MSP_WORKFLOW_STAGE_PDPS table pour afficher les informations sur les pages de détails de projet (PDP) dans les étapes du flux de travail.</span><span class="sxs-lookup"><span data-stu-id="aaf42-289">For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
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

## <a name="cleaning-up"></a><span data-ttu-id="aaf42-290">Nettoyage</span><span class="sxs-lookup"><span data-stu-id="aaf42-290">Cleaning up</span></span>
<span data-ttu-id="aaf42-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-291"></span></span>

<span data-ttu-id="aaf42-292">Une fois que vous avez testé certains exemples de code, il existe des objets d'entreprise et des paramètres qui doivent être supprimés ou réinitialisés.</span><span class="sxs-lookup"><span data-stu-id="aaf42-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="aaf42-293">Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`d'entreprise ().</span><span class="sxs-lookup"><span data-stu-id="aaf42-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="aaf42-294">Les liens de la page Paramètres du serveur vous permettent de supprimer les anciens éléments, de forcer l'archivage des projets, de gérer la file d'attente des travaux pour tous les utilisateurs et d'effectuer d'autres tâches d'administration.</span><span class="sxs-lookup"><span data-stu-id="aaf42-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="aaf42-295">Voici quelques-uns des liens figurant sur la page Paramètres du serveur que vous pouvez utiliser pour les activités de nettoyage classiques après l'exécution d'exemples de code:</span><span class="sxs-lookup"><span data-stu-id="aaf42-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="aaf42-296">**Champs personnalisés d’entreprise et tables de choix**</span><span class="sxs-lookup"><span data-stu-id="aaf42-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="aaf42-297">**Gérer les travaux en file d’attente**</span><span class="sxs-lookup"><span data-stu-id="aaf42-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="aaf42-298">**Supprimer des objets d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="aaf42-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="aaf42-299">**Forcer l'archivage des objets d'entreprise**</span><span class="sxs-lookup"><span data-stu-id="aaf42-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="aaf42-300">**Types de projets d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="aaf42-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="aaf42-301">**Phases du flux de travail**</span><span class="sxs-lookup"><span data-stu-id="aaf42-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="aaf42-302">**Étapes du flux de travail**</span><span class="sxs-lookup"><span data-stu-id="aaf42-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="aaf42-303">**Pages de détails de projet**</span><span class="sxs-lookup"><span data-stu-id="aaf42-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="aaf42-304">**Périodes de rapports de temps**</span><span class="sxs-lookup"><span data-stu-id="aaf42-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="aaf42-305">**Paramètres et valeurs par défaut de la feuille de temps**</span><span class="sxs-lookup"><span data-stu-id="aaf42-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="aaf42-306">**Classifications de ligne**</span><span class="sxs-lookup"><span data-stu-id="aaf42-306">**Line Classifications**</span></span>
    
<span data-ttu-id="aaf42-307">Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance Project Web App, et non par une page de paramètres de serveur Project Web App spécifique.</span><span class="sxs-lookup"><span data-stu-id="aaf42-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="aaf42-308">Dans l'application Administration centrale de SharePoint, choisissez **paramètres généraux**de l'application, choisissez **gérer** sous **paramètres de Project Server**, puis choisissez l'instance de Project Web App dans la liste déroulante de la page Paramètres du serveur. .</span><span class="sxs-lookup"><span data-stu-id="aaf42-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="aaf42-309">Par exemple, choisissez **gestionnaires d'événements côté serveur** pour ajouter ou supprimer des gestionnaires d'événements pour l'instance Project Web App sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="aaf42-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aaf42-310">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaf42-310">See also</span></span>
<span data-ttu-id="aaf42-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="aaf42-311"></span></span>

- [<span data-ttu-id="aaf42-312">Conditions préalables pour les exemples de code basés sur WCF</span><span class="sxs-lookup"><span data-stu-id="aaf42-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="aaf42-313">Utiliser l'emprunt d'identité avec WCF</span><span class="sxs-lookup"><span data-stu-id="aaf42-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="aaf42-314">Vue d’ensemble de la référence Project PSI</span><span class="sxs-lookup"><span data-stu-id="aaf42-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="aaf42-315">Centre pour développeurs SharePoint</span><span class="sxs-lookup"><span data-stu-id="aaf42-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

