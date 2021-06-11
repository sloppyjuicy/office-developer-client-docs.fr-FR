---
title: Séquences d’appels classiques OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Cette section décrit les séquences d’appels classiques Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité du fournisseur OSC, qu’un fournisseur OSC implémente.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413611"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="97b8a-103">Séquences d’appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="97b8a-103">OSC typical calling sequences</span></span>

<span data-ttu-id="97b8a-104">Cette section décrit les séquences d’appels classiques Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité du fournisseur OSC, qu’un fournisseur OSC implémente.</span><span class="sxs-lookup"><span data-stu-id="97b8a-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="97b8a-105">Les séquences d’appels classiques illustrent comment et quand OSC utilise ces interfaces et méthodes, pour vous aider à mieux déterminer comment implémenter un membre donné sur une interface d’extensibilité de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="97b8a-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="97b8a-106">La séquence d’appels réelle peut varier en fonction des fonctionnalités renvoyées par la méthode [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="97b8a-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="97b8a-107">Voici quelques exemples de fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="97b8a-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="97b8a-108">Prise en charge par les fournisseurs pour l’obtention, la mise en cache ou la recherche dynamique d’amis et d’activités à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="97b8a-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="97b8a-109">Interface utilisateur que l’OSC doit afficher pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97b8a-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="97b8a-110">Type d’authentification (par exemple, authentification basée sur les formulaires) que l’OSC doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="97b8a-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="97b8a-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="97b8a-111">In this section</span></span>

- <span data-ttu-id="97b8a-112">[Authentification](basic-authentication.md)de base : décrit la séquence d’appels classique de l’OSC pour prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification de base.</span><span class="sxs-lookup"><span data-stu-id="97b8a-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="97b8a-113">[](forms-based-authentication.md)Authentification basée sur les formulaires : décrit la séquence d’appels classique de l’OSC pour prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="97b8a-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="97b8a-114">[Obtention](getting-activities.md)d’activités : décrit la séquence d’appels classique de l’OSC pour synchroniser les activités des amis de l’utilisateur Office à partir d’un réseau social, si le fournisseur OSC du réseau social prend en charge la synchronisation des activités.</span><span class="sxs-lookup"><span data-stu-id="97b8a-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="97b8a-115">[Obtention d’informations](getting-friends-information.md)sur les amis : décrit la séquence d’appels classique de l’OSC pour synchroniser la liste des amis de l’utilisateur Office à partir d’un réseau social, si le fournisseur OSC du réseau social prend en charge la synchronisation des contacts mise en cache.</span><span class="sxs-lookup"><span data-stu-id="97b8a-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="97b8a-116">Référence</span><span class="sxs-lookup"><span data-stu-id="97b8a-116">Reference</span></span>

- [<span data-ttu-id="97b8a-117">Documentation de référence sur le fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="97b8a-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="97b8a-118">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="97b8a-118">Related sections</span></span>

- [<span data-ttu-id="97b8a-119">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="97b8a-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="97b8a-120">Exemples de modèles de OSC</span><span class="sxs-lookup"><span data-stu-id="97b8a-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="97b8a-121">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="97b8a-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="97b8a-122">Débogage d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="97b8a-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="97b8a-123">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="97b8a-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="97b8a-124">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="97b8a-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="97b8a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97b8a-125">See also</span></span>

- [<span data-ttu-id="97b8a-126">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="97b8a-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

