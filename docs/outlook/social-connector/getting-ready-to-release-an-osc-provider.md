---
title: Préparation à la publication d’un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section suggère des tests que vous pouvez faire avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414661"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="b8267-103">Préparation à la publication d’un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="b8267-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="b8267-104">Cette section suggère des tests que vous pouvez faire avant de libérer votre fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="b8267-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="b8267-105">Vous pouvez commencer à faire référence aux rubriques de cette section et effectuer certains de ces tests au cours de vos phases de développement et de test, mais vous devriez avoir effectué ces tests au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="b8267-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="b8267-106">Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces du fournisseur OSC par rapport aux fonctionnalités que vous spécifiez pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="b8267-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="b8267-107">En outre, même si OSC est une fonctionnalité partagée par plusieurs applications clientes Office, ces tests utilisent Outlook comme client pour tester les fonctionnalités fondamentales.</span><span class="sxs-lookup"><span data-stu-id="b8267-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="b8267-108">Vous devez déterminer si d’autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b8267-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b8267-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b8267-109">In this section</span></span>

- <span data-ttu-id="b8267-110">[Test du](testing-deployment.md)déploiement : décrit les scénarios que vous devez tester autour de l’installation et de la désinstallation d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="b8267-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="b8267-111">[Test des fonctionnalités,](testing-capabilities-authentication-and-configuration.md)de l’authentification et de la configuration : décrit les tests d’obtention des fonctionnalités et les scénarios de configuration d’un compte et d’authentification d’un utilisateur pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="b8267-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="b8267-112">[Test des](testing-following-and-stop-following-persons.md)personnes Stop-Following suivantes : décrit les scénarios pour tester la capacité du fournisseur OSC à ajouter une personne en tant qu’ami ou à supprimer un ami du réseau social.</span><span class="sxs-lookup"><span data-stu-id="b8267-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="b8267-113">[Testing Friends](testing-friends.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC renvoie correctement les données d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="b8267-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="b8267-114">[Activités de](testing-activities.md)test : décrit les tests et les scénarios pour vérifier que le fournisseur OSC renvoie correctement les activités d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="b8267-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="b8267-115">Référence</span><span class="sxs-lookup"><span data-stu-id="b8267-115">Reference</span></span>

- [<span data-ttu-id="b8267-116">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b8267-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="b8267-117">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="b8267-117">Related sections</span></span>

- [<span data-ttu-id="b8267-118">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="b8267-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="b8267-119">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="b8267-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="b8267-120">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="b8267-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="b8267-121">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b8267-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="b8267-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b8267-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

