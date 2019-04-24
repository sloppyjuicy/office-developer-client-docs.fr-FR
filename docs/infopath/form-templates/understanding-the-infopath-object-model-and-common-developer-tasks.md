---
title: Présentation du modèle objet InfoPath et des tâches développeur courantes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- examples [infopath 2007],InfoPath 2007, developer tasks,developer tasks [InfoPath 2007],InfoPath 2007, object models,object models [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: Cette section fournit des informations sur les tâches développeur courantes lors du développement de modèles de formulaires InfoPath utilisant du code managé.
ms.openlocfilehash: a84bf1a70407ca87e1a83f74856d363d8860d4a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303436"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="e4194-104">Présentation du modèle objet InfoPath et des tâches développeur courantes</span><span class="sxs-lookup"><span data-stu-id="e4194-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="e4194-105">Cette section fournit des informations sur les tâches développeur courantes lors du développement de modèles de formulaires InfoPath utilisant du code managé.</span><span class="sxs-lookup"><span data-stu-id="e4194-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="e4194-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e4194-106">In this section</span></span>

[<span data-ttu-id="e4194-107">Accéder aux données de l'application</span><span class="sxs-lookup"><span data-stu-id="e4194-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="e4194-108">Explique comment accéder aux informations concernant l'application InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4194-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="e4194-109">Répondre aux événements de formulaire</span><span class="sxs-lookup"><span data-stu-id="e4194-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="e4194-110">Présente la création de gestionnaires d'événements qui réagissent aux événements se produisant lorsque l'utilisateur remplit un formulaire.</span><span class="sxs-lookup"><span data-stu-id="e4194-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="e4194-111">Accéder aux données de formulaire</span><span class="sxs-lookup"><span data-stu-id="e4194-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="e4194-112">Présente la manière d'accéder aux informations sur le document XML sous-jacent du formulaire, les données qu'il contient ou d'effectuer des opérations sur le document XML.</span><span class="sxs-lookup"><span data-stu-id="e4194-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="e4194-113">Accéder à des sources de données externes</span><span class="sxs-lookup"><span data-stu-id="e4194-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="e4194-114">Présente la manière d'accéder à des données depuis des sources de données externes.</span><span class="sxs-lookup"><span data-stu-id="e4194-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="e4194-115">Écrire une logique conditionnelle qui détermine l'environnement d'exécution</span><span class="sxs-lookup"><span data-stu-id="e4194-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="e4194-116">Explique comment écrire du code qui effectue une action différente selon que le formulaire est ouvert dans InfoPath, un navigateur Web ou un navigateur mobile.</span><span class="sxs-lookup"><span data-stu-id="e4194-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="e4194-117">Utilisation des fenêtres de formulaire</span><span class="sxs-lookup"><span data-stu-id="e4194-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="e4194-118">Présente l'utilisation de fenêtres de formulaires</span><span class="sxs-lookup"><span data-stu-id="e4194-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="e4194-119">Utiliser les affichages</span><span class="sxs-lookup"><span data-stu-id="e4194-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="e4194-120">Présente l'utilisation de vues.</span><span class="sxs-lookup"><span data-stu-id="e4194-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="e4194-121">Utiliser des solutions hors ligne</span><span class="sxs-lookup"><span data-stu-id="e4194-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="e4194-122">Présente l'utilisation de solutions hors ligne.</span><span class="sxs-lookup"><span data-stu-id="e4194-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="e4194-123">Utiliser des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="e4194-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="e4194-124">Présente l'utilisation de signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="e4194-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="e4194-125">Gérer les erreurs</span><span class="sxs-lookup"><span data-stu-id="e4194-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="e4194-126">Présente la gestion des erreurs dans les projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="e4194-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="e4194-127">Utiliser les paramètres de gestion des droits relatifs à l'information</span><span class="sxs-lookup"><span data-stu-id="e4194-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="e4194-128">Présente l'utilisation des paramètres Gestion des droits relatifs à l'information (IRM).</span><span class="sxs-lookup"><span data-stu-id="e4194-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="e4194-129">Ajouter et référencer des assemblys personnalisés</span><span class="sxs-lookup"><span data-stu-id="e4194-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="e4194-130">Explique comment ajouter des assemblys personnalisés à un projet de modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="e4194-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

