---
title: Préparation de la publication d'un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section propose des tests que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327152"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="8afd8-103">Préparation de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="8afd8-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="8afd8-104">Cette section propose des tests que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="8afd8-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="8afd8-105">Vous pouvez commencer à vous référer aux rubriques de cette section et effectuer certains de ces tests pendant les phases de développement et de test, mais vous devez avoir effectué ces tests au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="8afd8-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="8afd8-106">Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces du fournisseur OSC en ce qui concerne les fonctionnalités que vous spécifiez pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8afd8-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="8afd8-107">Par ailleurs, même si OSC est une fonctionnalité partagée par plusieurs applications clientes Office, ces tests utilisent Outlook comme client pour tester les fonctionnalités fondamentales.</span><span class="sxs-lookup"><span data-stu-id="8afd8-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="8afd8-108">Vous devez déterminer si d'autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8afd8-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="8afd8-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="8afd8-109">In this section</span></span>

- <span data-ttu-id="8afd8-110">[Test du déploiement](testing-deployment.md): décrit les scénarios que vous devez tester pour l'installation et la désinstallation d'un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8afd8-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="8afd8-111">[Test des fonctionnalités, de l'authentification et](testing-capabilities-authentication-and-configuration.md)de la configuration: décrit les tests permettant d'obtenir des fonctionnalités, ainsi que les scénarios de configuration d'un compte et d'authentification d'un utilisateur pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="8afd8-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="8afd8-112">[Test suivi des personnes](testing-following-and-stop-following-persons.md)suivantes: décrit les scénarios permettant de tester la capacité du fournisseur OSC à ajouter une personne en tant qu'ami ou à supprimer un ami du réseau social.</span><span class="sxs-lookup"><span data-stu-id="8afd8-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="8afd8-113">[Test des amis](testing-friends.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC retourne correctement les données des amis et des non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8afd8-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="8afd8-114">[Activités de test](testing-activities.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC retourne correctement les activités des amis et des non-amis, le cas échéant, selon le mode de synchronisation pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8afd8-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="8afd8-115">Référence</span><span class="sxs-lookup"><span data-stu-id="8afd8-115">Reference</span></span>

- [<span data-ttu-id="8afd8-116">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="8afd8-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="8afd8-117">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="8afd8-117">Related sections</span></span>

- [<span data-ttu-id="8afd8-118">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="8afd8-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="8afd8-119">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="8afd8-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="8afd8-120">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="8afd8-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="8afd8-121">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="8afd8-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="8afd8-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="8afd8-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

