---
title: Création de modèles de formulaire à l'aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, creating,object models [InfoPath 2003], creating managed code form templates for InfoPath 2007,form templates [InfoPath 2007], creating InfoPath 2003-compatible
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: Cette section présente le code d'initialisation et de nettoyage, explique comment ajouter des gestionnaires d'événements, comment déboguer et déployer des modèles de formulaires InfoPath utilisant le modèle objet compatible avec InfoPath 2003 ; elle présente également la gestion des threads et l'utilisation de MSXML (Microsoft XML Core Services) à partir de solutions InfoPath avec code managé.
ms.openlocfilehash: 5069636dde87eb473a2b8bef4b58a6006d557085
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410531"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="ad373-104">Création de modèles de formulaire à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="ad373-105">Cette section présente le code d'initialisation et de nettoyage, explique comment ajouter des gestionnaires d'événements, comment déboguer et déployer des modèles de formulaires InfoPath utilisant le modèle objet compatible avec InfoPath 2003 ; elle présente également la gestion des threads et l'utilisation de MSXML (Microsoft XML Core Services) à partir de solutions InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="ad373-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ad373-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ad373-106">In this section</span></span>

[<span data-ttu-id="ad373-107">Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="ad373-108">Présente la création du code d'initialisation et de nettoyage dans les méthodes _Startup et _Shutdown de votre projet.</span><span class="sxs-lookup"><span data-stu-id="ad373-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="ad373-109">Ajout d'un gestionnaire d'événements à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="ad373-110">Présente l'ajout de gestionnaires d'événements et les attributs appliqués pour identifier les gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="ad373-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="ad373-111">DéBogage de projets InfoPath à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="ad373-112">Présente le débogage de projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="ad373-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="ad373-113">Déployer des modèles de formulaire InfoPath avec code</span><span class="sxs-lookup"><span data-stu-id="ad373-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="ad373-114">Présente le déploiement de projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="ad373-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="ad373-115">Prise en charge du threading dans les projets InfoPath à l'aide du modèle de projet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="ad373-116">Présente la gestion des threads dans les projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="ad373-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="ad373-117">Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ad373-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="ad373-118">Présente l'utilisation de code MSXML et System.Xml dans les projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="ad373-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

