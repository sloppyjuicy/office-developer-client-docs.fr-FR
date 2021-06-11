---
title: XML pour les fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'L’élément Capabilities du schéma XML du fournisseur (OSC) permet à un fournisseur OSC de spécifier ses fonctionnalités. Ces fonctionnalités incluent les fonctionnalités suivantes :'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435004"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="bbfe9-104">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="bbfe9-104">XML for capabilities</span></span>

<span data-ttu-id="bbfe9-105">**L’élément Capabilities** du schéma XML du fournisseur (OSC) permet à un fournisseur OSC de spécifier ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="bbfe9-106">Ces fonctionnalités incluent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbfe9-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="bbfe9-107">Si le fournisseur prend en charge l’obtention, la mise en cache ou la recherche dynamique d’amis et d’activités à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="bbfe9-108">La façon dont OSC doit afficher certaines interfaces utilisateur d’accès.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="bbfe9-109">Si l’OSC doit utiliser l’authentification basée sur les formulaires ou configurer automatiquement le réseau social et les journaux sur l’utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="bbfe9-110">Le schéma XML des **fonctionnalités** est essentiel car il identifie à l’OSC les fonctionnalités pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="bbfe9-111">Un fournisseur OSC doit implémenter la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) qui renvoie une  _chaîne de_ résultats.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="bbfe9-112">L’OSC appelle **ISocialProvider::GetCapabilities** pour obtenir des informations sur  les fonctionnalités du fournisseur OSC dans la chaîne de résultats, qui est conforme à la définition de schéma XML pour l’élément **capabilities.**</span><span class="sxs-lookup"><span data-stu-id="bbfe9-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="bbfe9-113">Ces informations permettent aux appels ultérieurs de l’OSC au fournisseur OSC de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="bbfe9-114">Pour spécifier les fonctionnalités d’un fournisseur OSC en tant que paramètre de sortie de la méthode **ISocialProvider::GetCapabilities,** vous devez vous conformer au schéma XML d’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="bbfe9-115">La figure suivante illustre **la** structure XML des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bbfe9-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="bbfe9-116">**Figure 1. \<fonctionnalités \> Structure XML**</span><span class="sxs-lookup"><span data-stu-id="bbfe9-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Structure XML des fonctionnalités](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="bbfe9-118">Pour obtenir des descriptions détaillées des éléments enfants de l’élément **capabilities,** voir [Capabilities XML Elements](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="bbfe9-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="bbfe9-119">Pour obtenir un exemple de **fonctionnalités** XML, voir [Capabilities XML Example](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="bbfe9-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="bbfe9-120">Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir Outlook [Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="bbfe9-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbfe9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbfe9-121">See also</span></span>

- [<span data-ttu-id="bbfe9-122">Exemple de fonctionnalités XML</span><span class="sxs-lookup"><span data-stu-id="bbfe9-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="bbfe9-123">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="bbfe9-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="bbfe9-124">XML pour les amis</span><span class="sxs-lookup"><span data-stu-id="bbfe9-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="bbfe9-125">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="bbfe9-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="bbfe9-126">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="bbfe9-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

