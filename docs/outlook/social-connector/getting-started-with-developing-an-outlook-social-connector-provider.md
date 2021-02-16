---
title: Mise en place du développement d’un fournisseur Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: La référence du fournisseur Outlook Social Connector (OSC) décrit comment développer un fournisseur OSC à l’aide de l’extensibilité du fournisseur OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327159"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="12de8-103">Mise en place du développement d’un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="12de8-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="12de8-104">La référence du fournisseur Outlook Social Connector (OSC) décrit comment développer un fournisseur OSC à l’aide de l’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="12de8-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="12de8-105">Si vous débutez dans le développement de solutions pour Outlook, voir Sélection d’une API ou d’une technologie pour le développement de [solutions Outlook](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) afin d’identifier les API et technologies les plus appropriées à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="12de8-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="12de8-106">Cette section donne une vue d’ensemble d’OSC, de la façon dont un fournisseur OSC peut être utile, des étapes rapides pour apprendre à développer un fournisseur, des exigences techniques, des meilleures pratiques pour le développement d’un fournisseur et des nouveautés de cette version.</span><span class="sxs-lookup"><span data-stu-id="12de8-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="12de8-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="12de8-107">In this section</span></span>

- <span data-ttu-id="12de8-108">Nouveautés pour les fournisseurs : compare les fonctionnalités OSC de la version précédente et actuelle, et décrit les membres de [l’interface](what-s-new-for-providers.md)et les éléments de schéma XML qui ont été ajoutés, modifiés ou supprimés dans cette version.</span><span class="sxs-lookup"><span data-stu-id="12de8-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="12de8-109">[Pourquoi développer un fournisseur Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md): décrit comment un fournisseur OSC peut être utile pour les sites de réseaux sociaux courants et d’autres outils réseau internes.</span><span class="sxs-lookup"><span data-stu-id="12de8-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="12de8-110">[Lien entre OSC et Outlook](relating-the-osc-with-outlook-and-social-networks.md)et les réseaux sociaux : fournit une vue architecturale de la façon dont OSC connecte les utilisateurs Outlook aux réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="12de8-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="12de8-111">Définit également la façon dont les termes courants, tels que « réseaux sociaux », « amis », « non-amis » et « contacts » sont utilisés dans le reste de cette référence.</span><span class="sxs-lookup"><span data-stu-id="12de8-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="12de8-112">[Étapes rapides pour apprendre à développer](quick-steps-for-learning-to-develop-a-provider.md)un fournisseur : fournit un résumé des étapes à suivre pour apprendre à développer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="12de8-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="12de8-113">[Exigences techniques](technical-requirements.md): décrit les langages de programmation pris en charge, les exigences de visibilité COM, les exigences de type de retour de méthode et les détails de la DLL d’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="12de8-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="12de8-114">[Meilleures pratiques pour le développement d’un](best-practices-for-developing-a-provider.md)fournisseur : fournit une liste des meilleures pratiques à suivre lors du développement d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="12de8-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="12de8-115">Référence</span><span class="sxs-lookup"><span data-stu-id="12de8-115">Reference</span></span>

- [<span data-ttu-id="12de8-116">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="12de8-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="12de8-117">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="12de8-117">Related sections</span></span>

- [<span data-ttu-id="12de8-118">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="12de8-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="12de8-119">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="12de8-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="12de8-120">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="12de8-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="12de8-121">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="12de8-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="12de8-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="12de8-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="12de8-123">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="12de8-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="12de8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12de8-124">See also</span></span>

- [<span data-ttu-id="12de8-125">Microsoft Outlook Social Connector 32 bits</span><span class="sxs-lookup"><span data-stu-id="12de8-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="12de8-126">Mise à jour pour Outlook Social Connector (KB983403), édition 32 bits</span><span class="sxs-lookup"><span data-stu-id="12de8-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="12de8-127">Mise à jour pour Outlook Social Connector (KB983403), édition 64 bits</span><span class="sxs-lookup"><span data-stu-id="12de8-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="12de8-128">Outlook Social Connector 2013 : Modèles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="12de8-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

