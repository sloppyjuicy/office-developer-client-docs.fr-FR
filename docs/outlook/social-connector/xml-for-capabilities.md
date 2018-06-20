---
title: Fichier XML pour les fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'L’élément capabilities dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC spécifier ses fonctionnalités. Ces fonctionnalités sont les suivantes :'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787707"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="f2457-104">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f2457-104">XML for capabilities</span></span>

<span data-ttu-id="f2457-105">L’élément **capabilities** dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC spécifier ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="f2457-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="f2457-106">Ces fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f2457-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="f2457-107">Si le fournisseur prend en charge l’obtention, la mise en cache ou recherchez dynamiquement des amis et des activités à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="f2457-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="f2457-108">Comment l’OSC doit afficher certaines des interfaces utilisateur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f2457-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="f2457-109">Si l’OSC doit utiliser l’authentification basée sur les formulaires ou configurer automatiquement les réseaux sociaux et les journaux de l’utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="f2457-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="f2457-110">Le schéma XML pour les **fonctionnalités** d’est essentiel car il identifie l’OSC les fonctionnalités prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f2457-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="f2457-111">Un fournisseur OSC doit implémenter la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) qui renvoie une chaîne de _résultat_ .</span><span class="sxs-lookup"><span data-stu-id="f2457-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="f2457-112">L’OSC appelle **ISocialProvider::GetCapabilities** pour obtenir des informations sur les fonctionnalités du fournisseur OSC dans la chaîne de _résultat_ , qui est conforme à la définition de schéma XML pour l’élément **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="f2457-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="f2457-113">Ces informations permettent les appels suivants à partir de l’OSC au fournisseur OSC fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="f2457-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="f2457-114">Pour spécifier les fonctionnalités d’un fournisseur OSC comme paramètre de sortie de la méthode **ISocialProvider::GetCapabilities** , vous devez vous conformer au schéma XML OSC fournisseur extensibilité.</span><span class="sxs-lookup"><span data-stu-id="f2457-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="f2457-115">La figure suivante illustre la structure XML des **capacités** .</span><span class="sxs-lookup"><span data-stu-id="f2457-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="f2457-116">**La figure 1. \<fonctionnalités\> structure XML**</span><span class="sxs-lookup"><span data-stu-id="f2457-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Structure XML des fonctionnalités](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="f2457-118">Pour obtenir des descriptions détaillées des éléments enfants de l’élément de **fonctionnalités** , voir [Fonctionnalités des éléments XML](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="f2457-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="f2457-119">Pour obtenir un exemple de **fonctionnalités** XML, voir [Exemple de code XML des capacités](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="f2457-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="f2457-120">Pour une définition complète du schéma XML de fournisseur OSC, y compris les éléments qui sont obligatoires ou facultatives, voir [Schéma du XML fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="f2457-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2457-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2457-121">See also</span></span>

- [<span data-ttu-id="f2457-122">Exemple de code XML des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f2457-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="f2457-123">Synchronisation de vos amis et activités</span><span class="sxs-lookup"><span data-stu-id="f2457-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="f2457-124">Code XML des amis</span><span class="sxs-lookup"><span data-stu-id="f2457-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="f2457-125">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="f2457-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="f2457-126">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="f2457-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

