---
title: Étapes rapides pour apprendre à développer un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Cette rubrique propose quelques étapes pour vous familiariser avec le développement d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329217"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="25628-103">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25628-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="25628-104">Pour développer un fournisseur OSC, vous devez effectuer les étapes générales suivantes:</span><span class="sxs-lookup"><span data-stu-id="25628-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="25628-105">Implémentez les quatre interfaces obligatoires: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)et [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="25628-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="25628-106">En fonction de la prise en charge de votre réseau social concernant la mise en cache des informations d'identification de connexion, le suivi d'une personne sur le réseau social ou la synchronisation dynamique des amis et de leurs activités, vous pouvez implémenter l'interface [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="25628-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="25628-107">Parallèlement aux interfaces d'implémentation, testez et déboguez le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25628-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="25628-108">Déployez le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25628-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="25628-109">Effectuer les tests finaux avant la publication.</span><span class="sxs-lookup"><span data-stu-id="25628-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="25628-110">Étape A: implémentation d'interfaces</span><span class="sxs-lookup"><span data-stu-id="25628-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="25628-111">Un fournisseur OSC implémente des interfaces afin que le OSC puisse utiliser ces interfaces pour obtenir les informations nécessaires concernant ou à partir du réseau social, via le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25628-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="25628-112">Ces informations incluent les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="25628-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="25628-113">Présenter la boîte de dialogue de connexion à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="25628-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="25628-114">Si le fournisseur prend en charge l'affichage des amis ou des activités tel qu'il est affiché sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="25628-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="25628-115">Comment afficher des amis et des activités dans la carte de visite ou dans le volet de contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="25628-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="25628-116">Quand actualiser les informations des amis ou des activités sur la carte de visite ou le volet des personnes.</span><span class="sxs-lookup"><span data-stu-id="25628-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="25628-117">Les informations sont généralement transmises du fournisseur au OSC, sous la forme de chaînes XML, en tant que paramètres de sortie des méthodes d'interface.</span><span class="sxs-lookup"><span data-stu-id="25628-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="25628-118">Les fournisseurs OSC et OSC sont conformes au schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25628-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="25628-119">Par conséquent, dans le cadre de l'implémentation des interfaces, vous avez besoin d'une bonne compréhension de la façon dont le schéma XML vous permet de spécifier des informations comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="25628-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="25628-120">Les ressources suivantes expliquent comment spécifier le code XML pour les fonctionnalités, les amis et les activités du fournisseur:</span><span class="sxs-lookup"><span data-stu-id="25628-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="25628-121">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="25628-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="25628-122">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="25628-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="25628-123">Exemple de XML de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="25628-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="25628-124">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="25628-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="25628-125">Exemple de code XML pour les amis</span><span class="sxs-lookup"><span data-stu-id="25628-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="25628-126">XML pour les amis</span><span class="sxs-lookup"><span data-stu-id="25628-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="25628-127">Exemple de XML d'informations sur les activités</span><span class="sxs-lookup"><span data-stu-id="25628-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="25628-128">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="25628-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="25628-129">Avant de commencer l'implémentation, consultez les rubriques suivantes pour gagner du temps lors du processus de débogage:</span><span class="sxs-lookup"><span data-stu-id="25628-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="25628-130">Exigences techniques</span><span class="sxs-lookup"><span data-stu-id="25628-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="25628-131">Meilleures pratiques pour le développement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25628-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="25628-132">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="25628-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="25628-133">Étape B: débogage</span><span class="sxs-lookup"><span data-stu-id="25628-133">Step B: Debugging</span></span>

<span data-ttu-id="25628-134">Le débogage d' [un fournisseur](debugging-a-provider.md) suggère des procédures de débogage que vous pouvez utiliser lors du développement d'un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25628-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="25628-135">Lors du développement, vous pouvez également vous reporter à la préparation de la [publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md) pour mieux comprendre le comportement attendu dans certains scénarios (par exemple, l'authentification de base et l'authentification basée sur les formulaires).</span><span class="sxs-lookup"><span data-stu-id="25628-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="25628-136">Étape C: déploiement</span><span class="sxs-lookup"><span data-stu-id="25628-136">Step C: Deploying</span></span>

<span data-ttu-id="25628-137">Consultez les rubriques suivantes pour en savoir plus sur les exigences en matière de déploiement:</span><span class="sxs-lookup"><span data-stu-id="25628-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="25628-138">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25628-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="25628-139">Inscription d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25628-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="25628-140">Liste de vérification de l'installation</span><span class="sxs-lookup"><span data-stu-id="25628-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="25628-141">Étape D: test final avant la publication</span><span class="sxs-lookup"><span data-stu-id="25628-141">Step D: Final testing before release</span></span>

<span data-ttu-id="25628-142">En fonction de votre réseau social et du fournisseur OSC, il existe généralement des tests spécifiques au fournisseur que vous devez effectuer avant de libérer votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="25628-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="25628-143">Pour obtenir une liste de tests suggérés, consultez la rubrique [préparation à la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="25628-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25628-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25628-144">See also</span></span>

- [<span data-ttu-id="25628-145">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="25628-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

