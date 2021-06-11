---
title: Développement d’un fournisseur avec le schéma XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations transmises d’un réseau social via le fournisseur OSC du réseau à OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539254"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="25d8a-103">Développement d’un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="25d8a-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="25d8a-104">Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations transmises d’un réseau social via le fournisseur OSC du réseau à OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="25d8a-105">Le schéma XML permet à un fournisseur OSC de spécifier les fonctionnalités du fournisseur, des amis et des éléments de flux d’activités sur le réseau social, à l’aide des trois principaux **éléments,** fonctionnalités **,** amis et **activityFeed** et leurs éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="25d8a-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="25d8a-106">Le fournisseur OSC implémente des interfaces et leurs méthodes dans l’extensibilité du fournisseur OSC, renvoyant des chaînes XML en tant que paramètres de sortie conformes au schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="25d8a-107">L’OSC appelle ces méthodes pour obtenir des informations qu’il peut comprendre telles que définies par le schéma XML.</span><span class="sxs-lookup"><span data-stu-id="25d8a-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="25d8a-108">L’extensibilité du fournisseur OSC prend en charge le débogage des fournisseurs en fixant la valeur de la clé de Registre `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` sur 1.</span><span class="sxs-lookup"><span data-stu-id="25d8a-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="25d8a-109">Lorsque vous allumez le débogage de fournisseur, l’OSC valide le XML du fournisseur par rapport à la version du schéma XML OSC que vous spécifiez dans l’attribut XML **xmlns.**</span><span class="sxs-lookup"><span data-stu-id="25d8a-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="25d8a-110">Pour OSC 1.1 et les versions de l’OSC depuis Outlook Social Connector 2013, spécifiez l’attribut **xmlns** comme suit :`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="25d8a-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="25d8a-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="25d8a-111">In this section</span></span>

- <span data-ttu-id="25d8a-112">[Synchronisation des amis et](synchronizing-friends-and-activities.md)des activités : décrit les différentes façons dont les fournisseurs OSC peuvent synchroniser des amis, des amis et des activités sur un réseau social.</span><span class="sxs-lookup"><span data-stu-id="25d8a-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="25d8a-113">Exemples XML de fournisseur OSC : inclut des exemples XML qui montrent comment spécifier les fonctionnalités d’un fournisseur [OSC,](osc-provider-xml-examples.md)des amis et des éléments de flux d’activités sur un réseau social à l’aide du schéma XML OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="25d8a-114">[XML](xml-for-capabilities.md)pour les fonctionnalités : explique la méthode [- ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que l’OSC utilise pour obtenir des informations sur les fonctionnalités, exprimées en **XML** de fonctionnalités, auprès du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="25d8a-115">Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier ses fonctionnalités, y compris la façon dont il authentifier les utilisateurs et synchronise les amis et les activités.</span><span class="sxs-lookup"><span data-stu-id="25d8a-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="25d8a-116">[XML pour les](xml-for-friends.md)amis : donne des exemples d’API que l’OSC utilise pour obtenir les informations des amis, exprimées en **XML** d’amis, auprès du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="25d8a-117">Cette section décrit également les éléments du XML **amis.**</span><span class="sxs-lookup"><span data-stu-id="25d8a-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="25d8a-118">[XML pour](xml-for-activities.md)les activités : donne des exemples d’API que l’OSC utilise pour obtenir des informations sur les activités, exprimées dans **activityFeed** XML, auprès du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="25d8a-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="25d8a-119">Cette section décrit également les éléments XML du schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier un flux d’activités.</span><span class="sxs-lookup"><span data-stu-id="25d8a-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="25d8a-120">Un flux d’activités inclut le réseau d’origine des éléments de flux d’activités, les détails de chaque élément de flux d’activités (par exemple, propriétaire, type et date de publication de l’activité) et le modèle d’affichage de l’activité.</span><span class="sxs-lookup"><span data-stu-id="25d8a-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="25d8a-121">Référence</span><span class="sxs-lookup"><span data-stu-id="25d8a-121">Reference</span></span>

- [<span data-ttu-id="25d8a-122">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="25d8a-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="25d8a-123">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="25d8a-123">Related sections</span></span>

- [<span data-ttu-id="25d8a-124">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="25d8a-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="25d8a-125">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="25d8a-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="25d8a-126">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="25d8a-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="25d8a-127">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25d8a-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="25d8a-128">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25d8a-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="25d8a-129">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25d8a-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="25d8a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25d8a-130">See also</span></span>

- [<span data-ttu-id="25d8a-131">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="25d8a-131">Debugging a Provider</span></span>](debugging-a-provider.md)

