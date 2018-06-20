---
title: Prise en main de publication d’un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section propose des tests, que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787584"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="d7e57-103">Prise en main de publication d’un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="d7e57-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="d7e57-104">Cette section propose des tests, que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d7e57-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="d7e57-105">Vous pouvez démarrer la référence pour les rubriques de cette section et procéder à certains de ces tests pendant le développement et les phases de test, mais vous devez avoir effectué ces tests au moment où que vous relâchez.</span><span class="sxs-lookup"><span data-stu-id="d7e57-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="d7e57-106">Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces de fournisseur OSC en ce qui concerne les fonctionnalités que vous spécifiez pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d7e57-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="d7e57-107">En outre, même si l’OSC est une fonctionnalité partagée par plusieurs applications clientes d’Office, ces tests utilisent Outlook comme client pour tester la fonctionnalité fondamentale.</span><span class="sxs-lookup"><span data-stu-id="d7e57-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="d7e57-108">Vous devez déterminer si les autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d7e57-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d7e57-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d7e57-109">In this section</span></span>

- <span data-ttu-id="d7e57-110">[Test du déploiement](testing-deployment.md): décrit les scénarios, vous devez tester autour de l’installation et de désinstallation d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d7e57-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="d7e57-111">[Test des fonctionnalités, l’authentification et la Configuration](testing-capabilities-authentication-and-configuration.md): description des tests pour obtenir les fonctionnalités et les scénarios de configuration d’un compte et l’authentification d’un utilisateur pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7e57-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="d7e57-112">[Personnes Stop-suivantes et les tests suivants](testing-following-and-stop-following-persons.md): décrit les scénarios pour tester la capacité du fournisseur OSC pour ajouter une personne comme un ami, ou pour supprimer un ami à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7e57-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="d7e57-113">[Test des amis](testing-friends.md): décrit les scénarios pour vérifier que le fournisseur OSC renvoie correctement les données des amis et non-amis, le cas échéant, selon le mode de synchronisation que le fournisseur prend en charge et les tests.</span><span class="sxs-lookup"><span data-stu-id="d7e57-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="d7e57-114">[Activités de test](testing-activities.md): décrit les scénarios pour vérifier que le fournisseur OSC renvoie correctement les activités des amis et non-amis, le cas échéant, selon le mode de synchronisation que le fournisseur prend en charge et les tests.</span><span class="sxs-lookup"><span data-stu-id="d7e57-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="d7e57-115">R�f�rence</span><span class="sxs-lookup"><span data-stu-id="d7e57-115">Reference</span></span>

- [<span data-ttu-id="d7e57-116">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d7e57-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="d7e57-117">Sections associées</span><span class="sxs-lookup"><span data-stu-id="d7e57-117">Related sections</span></span>

- [<span data-ttu-id="d7e57-118">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="d7e57-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="d7e57-119">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="d7e57-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="d7e57-120">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="d7e57-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="d7e57-121">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="d7e57-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="d7e57-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="d7e57-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

