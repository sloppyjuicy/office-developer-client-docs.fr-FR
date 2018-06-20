---
title: Séquences d’appel classiques OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Cette section décrit les séquences d’appel par défaut Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité de fournisseur OSC, qui implémente un fournisseur OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787697"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="350cd-103">Séquences d’appel classiques OSC</span><span class="sxs-lookup"><span data-stu-id="350cd-103">OSC typical calling sequences</span></span>

<span data-ttu-id="350cd-104">Cette section décrit les séquences d’appel par défaut Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité de fournisseur OSC, qui implémente un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="350cd-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="350cd-105">Les séquences d’appel classiques illustrent comment et quand l’OSC utilise ces interfaces et méthodes, pour vous permettre de mieux déterminent comment mettre en œuvre un membre donné sur une interface d’extensibilité de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="350cd-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="350cd-106">La séquence d’appel réelle peut varier selon les fonctionnalités renvoyées par la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="350cd-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="350cd-107">Exemples de fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="350cd-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="350cd-108">Fournisseur prend en charge pour l’obtention, la mise en cache ou recherchez dynamiquement des amis et des activités à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="350cd-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="350cd-109">L’interface utilisateur qui doit s’afficher l’OSC pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="350cd-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="350cd-110">Le type d’authentification (par exemple, l’authentification par formulaire) que l’OSC doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="350cd-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="350cd-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="350cd-111">In this section</span></span>

- <span data-ttu-id="350cd-112">[L’authentification de base](basic-authentication.md): décrit la séquence d’appel par défaut de l’OSC pour prendre en charge d’un utilisateur d’Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification de base.</span><span class="sxs-lookup"><span data-stu-id="350cd-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="350cd-113">[L’authentification basée sur les formulaires](forms-based-authentication.md): décrit la séquence d’appel par défaut de l’OSC pour prendre en charge d’un utilisateur d’Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="350cd-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="350cd-114">[Obtention des activités](getting-activities.md): décrit la séquence d’appel par défaut de l’OSC pour synchroniser les activités de vos amis de l’utilisateur d’Office à partir d’un réseau social, si le fournisseur OSC de réseau social prend en charge la synchronisation des activités.</span><span class="sxs-lookup"><span data-stu-id="350cd-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="350cd-115">[Obtention d’informations sur des amis](getting-friends-information.md): décrit la séquence d’appel par défaut de l’OSC de synchroniser la liste d’amis de l’utilisateur d’Office à partir d’un réseau social, si le fournisseur OSC de réseau social prend en charge la mise en cache la synchronisation des contacts.</span><span class="sxs-lookup"><span data-stu-id="350cd-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="350cd-116">R�f�rence</span><span class="sxs-lookup"><span data-stu-id="350cd-116">Reference</span></span>

- [<span data-ttu-id="350cd-117">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="350cd-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="350cd-118">Sections associées</span><span class="sxs-lookup"><span data-stu-id="350cd-118">Related sections</span></span>

- [<span data-ttu-id="350cd-119">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="350cd-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="350cd-120">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="350cd-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="350cd-121">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="350cd-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="350cd-122">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="350cd-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="350cd-123">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="350cd-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="350cd-124">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="350cd-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="350cd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="350cd-125">See also</span></span>

- [<span data-ttu-id="350cd-126">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="350cd-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

