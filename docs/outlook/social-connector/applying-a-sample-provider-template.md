---
title: Application d’un exemple de modèle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Les exemples Outlook de fournisseurs OSC (Social Connector) vous donnent une infrastructure pour l’implémentation d’un fournisseur OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425910"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="e1fea-103">Application d’un exemple de modèle de fournisseur</span><span class="sxs-lookup"><span data-stu-id="e1fea-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="e1fea-104">Les exemples Outlook de fournisseurs OSC (Social Connector) vous donnent une infrastructure pour l’implémentation d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="e1fea-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="e1fea-105">Les modèles de fournisseur sont disponibles en C++, C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1fea-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="e1fea-106">Ces modèles ne sont qu’un point de départ pour le développement de votre fournisseur . les modèles n’abordent pas l’écriture du code d’implémentation pour le fournisseur et la création d’un package d’installation pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e1fea-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="e1fea-107">La procédure suivante montre comment appliquer un modèle de fournisseur OSC lorsque vous commencez à développer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e1fea-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="e1fea-108">Pour appliquer un modèle de fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="e1fea-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="e1fea-109">Dans le menu **Démarrer,** cliquez avec le **bouton droit Microsoft Visual Studio 2010** et cliquez sur la commande Exécuter **en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="e1fea-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="e1fea-110">À l’invite, cliquez sur **Oui** pour exécuter Visual Studio en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e1fea-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="e1fea-111">Modifiez le nom et l’espace de noms du projet dans le modèle en identifiants de nom de projet et d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e1fea-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="e1fea-112">Modifiez la **classe AssemblyInfo** pour spécifier les informations d’assembly appropriées.</span><span class="sxs-lookup"><span data-stu-id="e1fea-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="e1fea-113">Implémentez les membres de l’interface **marqués comme To-Do** et ajoutez d’autres dépendances et références, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="e1fea-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="e1fea-114">Créez le projet.</span><span class="sxs-lookup"><span data-stu-id="e1fea-114">Build the project.</span></span>
    
6. <span data-ttu-id="e1fea-115">Assurez-vous que le ProgID de l’assembly du fournisseur est répertorié en tant que clé sous  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .</span><span class="sxs-lookup"><span data-stu-id="e1fea-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="e1fea-116">Pour distribuer le projet d’installation, créez un projet d’installation Visual Studio ou un outil d’installation de votre choix.</span><span class="sxs-lookup"><span data-stu-id="e1fea-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="e1fea-117">Votre projet d’installation doit terminer l’inscription COM pour votre assembly et également créer la clé ProgID comme répertorié à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="e1fea-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1fea-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fea-118">See also</span></span>

- [<span data-ttu-id="e1fea-119">Téléchargement des exemples</span><span class="sxs-lookup"><span data-stu-id="e1fea-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="e1fea-120">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="e1fea-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

