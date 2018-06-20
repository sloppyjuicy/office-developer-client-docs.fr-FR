---
title: Étapes rapides pour apprendre à développer un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Cette rubrique suggère quelques étapes pour en savoir plus sur le développement d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787704"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="5c0a5-103">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5c0a5-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="5c0a5-104">Pour développer un fournisseur OSC, vous devez effectuer les étapes générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c0a5-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="5c0a5-105">Implémenter les interfaces obligatoires quatre : [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)et [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5c0a5-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="5c0a5-106">En fonction de la prise en charge de votre réseau social pour la mise en cache des informations d’identification d’ouverture de session, suivi d’une personne sur le réseau social, ou dynamiquement synchronisation amis et leurs activités, vous souhaiterez mettre en œuvre l’interface [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0a5-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="5c0a5-107">Parallèlement à implémenter des interfaces, tester et déboguer le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="5c0a5-108">Déployer le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="5c0a5-109">Effectuer un test final avant le lancement.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="5c0a5-110">Étape a : implémenter des interfaces</span><span class="sxs-lookup"><span data-stu-id="5c0a5-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="5c0a5-111">Un fournisseur OSC implémente des interfaces afin que le OSC permettre utiliser ces interfaces pour obtenir les informations nécessaires sur ou à partir du réseau social, via le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="5c0a5-112">Ces informations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c0a5-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="5c0a5-113">Comment présenter la boîte de dialogue compte d’ouverture de session à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="5c0a5-114">Si le fournisseur prend en charge affichant amis ou activités telle qu’elle apparaît sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="5c0a5-115">Mode d’affichage des amis et des activités dans la carte de visite ou le volet personnes.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="5c0a5-116">Heure d’actualiser des amis ou des activités d’informations sur la carte de visite ou le volet personnes.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="5c0a5-117">Les informations sont généralement passées à partir du fournisseur à l’OSC, sous la forme de chaînes XML en tant que paramètres de sortie de méthodes d’interface.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="5c0a5-118">À la fois l’OSC et un fournisseur OSC respectent le schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="5c0a5-119">Par conséquent, au cours de l’implémentation des interfaces, vous devez bien comprendre comment le schéma XML permet de spécifier les informations comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="5c0a5-120">Les ressources suivantes expliquent comment spécifier le code XML pour les activités, amis et des fonctionnalités du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="5c0a5-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="5c0a5-121">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="5c0a5-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="5c0a5-122">Synchronisation de vos amis et activités</span><span class="sxs-lookup"><span data-stu-id="5c0a5-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="5c0a5-123">Exemple de code XML des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="5c0a5-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="5c0a5-124">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="5c0a5-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="5c0a5-125">Exemple de code XML amis</span><span class="sxs-lookup"><span data-stu-id="5c0a5-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="5c0a5-126">Code XML des amis</span><span class="sxs-lookup"><span data-stu-id="5c0a5-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="5c0a5-127">Exemple de flux XML d’activité</span><span class="sxs-lookup"><span data-stu-id="5c0a5-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="5c0a5-128">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="5c0a5-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="5c0a5-129">Avant de commencer la mise en œuvre, consultez également les rubriques suivantes pour gagner du temps plus loin dans le processus de débogage :</span><span class="sxs-lookup"><span data-stu-id="5c0a5-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="5c0a5-130">Conditions techniques</span><span class="sxs-lookup"><span data-stu-id="5c0a5-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="5c0a5-131">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5c0a5-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="5c0a5-132">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="5c0a5-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="5c0a5-133">Étape b : débogage</span><span class="sxs-lookup"><span data-stu-id="5c0a5-133">Step B: Debugging</span></span>

<span data-ttu-id="5c0a5-134">La rubrique [débogage d’un fournisseur](debugging-a-provider.md) suggère les procédures que vous pouvez utiliser lors du développement d’un fournisseur OSC de débogage.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="5c0a5-135">Lors du développement, vous pouvez également vous reporter à [Préparation pour la publication d’un fournisseur OSC](getting-ready-to-release-an-osc-provider.md) à mieux comprendre le comportement attendu dans certains scénarios (par exemple, l’authentification basée sur les formulaires et de base).</span><span class="sxs-lookup"><span data-stu-id="5c0a5-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="5c0a5-136">Étape c : déploiement</span><span class="sxs-lookup"><span data-stu-id="5c0a5-136">Step C: Deploying</span></span>

<span data-ttu-id="5c0a5-137">Voir les rubriques suivantes pour en savoir plus sur les exigences de déploiement :</span><span class="sxs-lookup"><span data-stu-id="5c0a5-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="5c0a5-138">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5c0a5-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="5c0a5-139">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5c0a5-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="5c0a5-140">Aide-mémoire d’installation</span><span class="sxs-lookup"><span data-stu-id="5c0a5-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="5c0a5-141">Étape d : Final test avant la publication</span><span class="sxs-lookup"><span data-stu-id="5c0a5-141">Step D: Final testing before release</span></span>

<span data-ttu-id="5c0a5-142">En fonction de votre réseau social et le fournisseur OSC, il existe des tests généralement spécifiques au fournisseur que vous devez effectuer avant de libérer votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="5c0a5-143">Pour une liste de suggestion de tests, voir [Préparation pour la publication d’un fournisseur OSC](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5c0a5-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c0a5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c0a5-144">See also</span></span>

- [<span data-ttu-id="5c0a5-145">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="5c0a5-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

