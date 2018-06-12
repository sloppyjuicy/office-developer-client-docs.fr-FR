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
ms.openlocfilehash: 9f0bbf36b2533b12ca3f31100c3abc21173d7c6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782463"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="07aab-104">Présentation du modèle objet InfoPath et des tâches développeur courantes</span><span class="sxs-lookup"><span data-stu-id="07aab-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="07aab-105">Cette section fournit des informations sur les tâches développeur courantes lors du développement de modèles de formulaires InfoPath utilisant du code managé.</span><span class="sxs-lookup"><span data-stu-id="07aab-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="07aab-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="07aab-106">In this section</span></span>

[<span data-ttu-id="07aab-107">Accès aux données d’Application</span><span class="sxs-lookup"><span data-stu-id="07aab-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="07aab-108">Explique comment accéder aux informations concernant l'application InfoPath.</span><span class="sxs-lookup"><span data-stu-id="07aab-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="07aab-109">Répondre aux événements de formulaire</span><span class="sxs-lookup"><span data-stu-id="07aab-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="07aab-110">Présente la création de gestionnaires d'événements qui réagissent aux événements se produisant lorsque l'utilisateur remplit un formulaire.</span><span class="sxs-lookup"><span data-stu-id="07aab-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="07aab-111">Accéder aux données de formulaire</span><span class="sxs-lookup"><span data-stu-id="07aab-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="07aab-112">Présente la manière d'accéder aux informations sur le document XML sous-jacent du formulaire, les données qu'il contient ou d'effectuer des opérations sur le document XML.</span><span class="sxs-lookup"><span data-stu-id="07aab-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="07aab-113">Accès aux Sources de données externes</span><span class="sxs-lookup"><span data-stu-id="07aab-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="07aab-114">Présente la manière d'accéder à des données depuis des sources de données externes.</span><span class="sxs-lookup"><span data-stu-id="07aab-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="07aab-115">Écrire une logique conditionnelle qui détermine l’environnement d’exécution</span><span class="sxs-lookup"><span data-stu-id="07aab-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="07aab-116">Explique comment écrire du code qui effectue une action différente selon que le formulaire est ouvert dans InfoPath, un navigateur Web ou un navigateur mobile.</span><span class="sxs-lookup"><span data-stu-id="07aab-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="07aab-117">Fenêtres de formulaires</span><span class="sxs-lookup"><span data-stu-id="07aab-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="07aab-118">Présente l'utilisation de fenêtres de formulaires</span><span class="sxs-lookup"><span data-stu-id="07aab-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="07aab-119">Utilisation des vues</span><span class="sxs-lookup"><span data-stu-id="07aab-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="07aab-120">Présente l'utilisation de vues.</span><span class="sxs-lookup"><span data-stu-id="07aab-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="07aab-121">Travailler avec des Solutions en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="07aab-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="07aab-122">Présente l'utilisation de solutions hors ligne.</span><span class="sxs-lookup"><span data-stu-id="07aab-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="07aab-123">Utilisation de Signatures numériques</span><span class="sxs-lookup"><span data-stu-id="07aab-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="07aab-124">Présente l'utilisation de signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="07aab-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="07aab-125">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="07aab-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="07aab-126">Présente la gestion des erreurs dans les projets InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="07aab-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="07aab-127">Paramètres de travail avec les droits de gestion</span><span class="sxs-lookup"><span data-stu-id="07aab-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="07aab-128">Présente l'utilisation des paramètres Gestion des droits relatifs à l'information (IRM).</span><span class="sxs-lookup"><span data-stu-id="07aab-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="07aab-129">Ajouter et référencer des assemblys personnalisés</span><span class="sxs-lookup"><span data-stu-id="07aab-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="07aab-130">Explique comment ajouter des assemblys personnalisés à un projet de modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="07aab-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

