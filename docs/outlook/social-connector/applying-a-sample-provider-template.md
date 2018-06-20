---
title: Appliquer un modèle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Les exemples de modèles de fournisseur Outlook Social Connector (OSC) vous fournissent une infrastructure pour l’implémentation d’un fournisseur OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787569"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="31621-103">Appliquer un modèle de fournisseur</span><span class="sxs-lookup"><span data-stu-id="31621-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="31621-104">Les exemples de modèles de fournisseur Outlook Social Connector (OSC) vous fournissent une infrastructure pour l’implémentation d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="31621-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="31621-105">Les modèles du fournisseur sont disponibles en C++, Visual C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31621-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="31621-106">Ces modèles sont simplement un point de départ pour le développement de votre fournisseur ; les modèles ne répondent pas écrire le code d’implémentation pour le fournisseur et la création d’un package d’installation pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="31621-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="31621-107">La procédure suivante montre comment appliquer un modèle de fournisseur OSC lorsque vous commencez à développer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="31621-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="31621-108">Pour appliquer un modèle de fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="31621-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="31621-109">Dans le menu **Démarrer** , cliquez sur **Microsoft Visual Studio 2010** , cliquez sur la commande **Exécuter en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="31621-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="31621-110">Lorsque vous y êtes invité, cliquez sur **Oui** pour exécuter Visual Studio en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="31621-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="31621-111">Remplacez le nom du projet et l’espace de noms dans le modèle de votre nom et l’espace de noms des identificateurs de projet.</span><span class="sxs-lookup"><span data-stu-id="31621-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="31621-112">Modifiez la classe **AssemblyInfo** pour spécifier les informations d’assembly approprié.</span><span class="sxs-lookup"><span data-stu-id="31621-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="31621-113">Implémenter les membres de l’interface marqués comme étant **des tâches** et ajoutez les autres dépendances et les références, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="31621-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="31621-114">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="31621-114">Build the project.</span></span>
    
6. <span data-ttu-id="31621-115">Assurez-vous que l’assembly du fournisseur ProgID est répertorié en tant que clé sous `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="31621-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="31621-116">Pour distribuer le projet d’installation, créez un projet d’installation dans Visual Studio ou un outil de configuration de votre choix.</span><span class="sxs-lookup"><span data-stu-id="31621-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="31621-117">Votre projet d’installation doit effectuer l’enregistrement COM pour l’assembly et créer la clé ProgID comme indiqué à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="31621-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31621-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31621-118">See also</span></span>

- [<span data-ttu-id="31621-119">Téléchargement d’exemples</span><span class="sxs-lookup"><span data-stu-id="31621-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="31621-120">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="31621-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

