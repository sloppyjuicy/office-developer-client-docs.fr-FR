---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons, vous pouvez déboguer un fournisseur Outlook Social Connector (OSC) :'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386851"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="d2591-103">Débogage d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="d2591-103">Debugging a provider</span></span>

<span data-ttu-id="d2591-104">Il existe plusieurs façons, vous pouvez déboguer un fournisseur Outlook Social Connector (OSC) :</span><span class="sxs-lookup"><span data-stu-id="d2591-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="d2591-105">À l’aide de commandes de débogage dans le composant du ruban de l’interface utilisateur Office Fluent dans Outlook ou l’application Office cliente prise en charge de provoquer l’OSC effectuer des actions différentes.</span><span class="sxs-lookup"><span data-stu-id="d2591-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="d2591-106">À l’aide de Fiddler pour l’API de suivi des appels et XML envoyés entre un réseau social et son fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="d2591-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="d2591-107">Déboguer les boutons</span><span class="sxs-lookup"><span data-stu-id="d2591-107">Debug buttons</span></span>

<span data-ttu-id="d2591-108">L’extensibilité du fournisseur OSC offre la possibilité de débogage d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d2591-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="d2591-109">Pour déboguer un fournisseur, créez un `DebugProviders` une valeur de type DWORD dans le Registre Windows sous la `SocialConnector` clé (comme indiqué dans la ligne suivante) et définir le `DebugProviders` la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="d2591-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="d2591-110">Par défaut, le fournisseur de débogage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d2591-110">By default, provider debugging is off.</span></span> <span data-ttu-id="d2591-111">Si le `DebugProviders` valeur n’est pas présente, ou il est présent et défini sur une valeur de 0, le fournisseur de débogage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d2591-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="d2591-112">Si le fournisseur de débogage est activé, le OSC affiche une boîte de dialogue d’alerte avec des informations d’erreur détaillé lorsqu’une erreur se produit et valide tout fournisseur OSC XML par rapport au schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d2591-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="d2591-113">En fonction de l’espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l’aide de OSC 1.0 est validé par rapport au fichier de schéma 1.0 OSC, OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="d2591-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="d2591-114">Un fournisseur OSC développées à l’aide de OSC 1.1 ou ultérieure est validé par rapport au fichier de schéma, OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="d2591-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="d2591-115">Lorsque vous utilisez la `DebugProviders` valeur, l’alerte de débogage s’affiche pour les fournisseurs tous chargés au lieu d’un fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="d2591-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="d2591-116">Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez un `ShowDebugButtons` une valeur de type DWORD dans le Registre Windows sous la `SocialConnector` clé et définir le `ShowDebugButtons` la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="d2591-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="d2591-117">Pour masquer les boutons de barre de commande debug, définissez la `ShowDebugButtons` valeur à 0.</span><span class="sxs-lookup"><span data-stu-id="d2591-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="d2591-118">Pour Outlook 2010 et les applications clientes par rapport à Office 2013, les boutons de débogage apparaissent sous l’onglet **compléments** du ruban de l’Explorateur de solutions.</span><span class="sxs-lookup"><span data-stu-id="d2591-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="d2591-119">Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent dans la barre de commande standard de la fenêtre d’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="d2591-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="d2591-120">Le tableau suivant décrit les boutons de débogage.</span><span class="sxs-lookup"><span data-stu-id="d2591-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="d2591-121">**Bouton de débogage**</span><span class="sxs-lookup"><span data-stu-id="d2591-121">**Debug button**</span></span>|<span data-ttu-id="d2591-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d2591-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2591-123">Synchroniser les Contacts</span><span class="sxs-lookup"><span data-stu-id="d2591-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="d2591-124">Entraîne l’OSC demander le fournisseur OSC uniquement les contacts mis en cache.</span><span class="sxs-lookup"><span data-stu-id="d2591-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="d2591-125">Synchronisation de liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="d2591-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="d2591-126">Entraîne l’OSC remplir des données à partir de la liste d’adresses globale Exchange aux contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2591-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="d2591-127">Invalider le Cache de catégorie</span><span class="sxs-lookup"><span data-stu-id="d2591-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="d2591-128">Entraîne l’OSC recharger la liste des catégories pour chaque banque lorsque le flux d’activité est actualisé.</span><span class="sxs-lookup"><span data-stu-id="d2591-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="d2591-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="d2591-129">Fiddler</span></span>

<span data-ttu-id="d2591-130">Fiddler est un outil de débogage over-the-wire pour vérifier les appels d’API envoyés par votre fournisseur au réseau social et XML envoyées par le réseaux sociaux à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d2591-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="d2591-131">Fiddler est disponible pour téléchargement à l’adresse [Proxy de débogage Web Fiddler](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="d2591-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2591-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2591-132">See also</span></span>

- [<span data-ttu-id="d2591-133">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="d2591-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="d2591-134">Synchronisation de vos amis et activités</span><span class="sxs-lookup"><span data-stu-id="d2591-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="d2591-135">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="d2591-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="d2591-136">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="d2591-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="d2591-137">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="d2591-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="d2591-138">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="d2591-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

