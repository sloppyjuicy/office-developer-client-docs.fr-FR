---
title: Développement d’un fournisseur avec le schéma XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations qui sont transmises à partir d’un réseau social par le biais de fournisseur OSC du réseau à l’OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787592"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="79cce-103">Développement d’un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="79cce-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="79cce-104">Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations qui sont transmises à partir d’un réseau social par le biais de fournisseur OSC du réseau à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="79cce-105">Le schéma XML permet à un fournisseur OSC spécifier les fonctionnalités du fournisseur, amis, les informations des éléments sur le réseaux sociaux, en utilisant les trois éléments principaux, **fonctionnalités**, **amis**et **activityFeed**et leurs enfants sur les activités éléments.</span><span class="sxs-lookup"><span data-stu-id="79cce-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="79cce-106">Le fournisseur OSC implémente les interfaces et les méthodes de l’extensibilité de fournisseur OSC, retourner des chaînes de code XML en tant que paramètres de sortie qui respectent le schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="79cce-107">L’OSC appelle ces méthodes pour obtenir des informations qu’il peut comprendre tel que défini par le schéma XML.</span><span class="sxs-lookup"><span data-stu-id="79cce-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="79cce-108">Extensibilité du fournisseur OSC prend en charge des fournisseurs de débogage en définissant le `DebugProviders` valeur de la `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` clé de Registre sur 1.</span><span class="sxs-lookup"><span data-stu-id="79cce-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="79cce-109">Lorsque vous activez le débogage de fournisseur, le OSC valide le fournisseur XML par rapport à la version du schéma XML OSC que vous spécifiez dans l’attribut XML de **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="79cce-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="79cce-110">Pour OSC 1.1 et les versions de l’OSC depuis Outlook Social Connector 2013, spécifiez l’attribut **xmlns** comme suit :`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="79cce-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="79cce-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="79cce-111">In this section</span></span>

- <span data-ttu-id="79cce-112">[Synchronisation des amis et activités](synchronizing-friends-and-activities.md): décrit les différentes manières que fournisseurs OSC pouvant être synchronisés amis, non amis et des activités sur un réseau social.</span><span class="sxs-lookup"><span data-stu-id="79cce-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="79cce-113">[Exemples de code XML de fournisseur OSC](osc-provider-xml-examples.md): exemples XML inclut qui montrent comment spécifier les fonctionnalités d’un fournisseur OSC, amis et l’activité de flux éléments sur un réseau social à l’aide du schéma XML OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="79cce-114">[Fichier XML pour les fonctionnalités](xml-for-capabilities.md): explique-méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) qui l’OSC utilise pour obtenir des informations sur les fonctionnalités, exprimées en XML des **fonctionnalités** , à partir du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="79cce-115">Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC qui autorisent un fournisseur OSC spécifier ses fonctionnalités, y compris son authentifie les utilisateurs et synchronise les amis et les activités.</span><span class="sxs-lookup"><span data-stu-id="79cce-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="79cce-116">[Code XML des amis](xml-for-friends.md): fournit des exemples d’API qui l’OSC utilise pour obtenir des informations de vos amis, exprimées en **amis** XML, à partir du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="79cce-117">Cette section décrit également les éléments dans le XML **amis** .</span><span class="sxs-lookup"><span data-stu-id="79cce-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="79cce-118">[XML pour les activités](xml-for-activities.md): fournit des exemples d’API qui l’OSC utilise pour obtenir des informations sur des activités, exprimées en **activityFeed** XML, à partir du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="79cce-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="79cce-119">Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC autoriser un fournisseur OSC spécifier un flux d’activité.</span><span class="sxs-lookup"><span data-stu-id="79cce-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="79cce-120">Un flux d’activité inclut le réseau dans lequel les informations sur les activités à l’origine, les éléments de détails de chaque élément d’informations sur les activités (telles que le propriétaire, tapez et date de publication de l’activité) et le modèle pour afficher l’activité.</span><span class="sxs-lookup"><span data-stu-id="79cce-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="79cce-121">R�f�rence</span><span class="sxs-lookup"><span data-stu-id="79cce-121">Reference</span></span>

- [<span data-ttu-id="79cce-122">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="79cce-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="79cce-123">Sections associées</span><span class="sxs-lookup"><span data-stu-id="79cce-123">Related sections</span></span>

- [<span data-ttu-id="79cce-124">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="79cce-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="79cce-125">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="79cce-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="79cce-126">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="79cce-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="79cce-127">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="79cce-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="79cce-128">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="79cce-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="79cce-129">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="79cce-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="79cce-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79cce-130">See also</span></span>

- [<span data-ttu-id="79cce-131">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="79cce-131">Debugging a Provider</span></span>](debugging-a-provider.md)

