---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281068"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="54f66-103">Débogage d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="54f66-103">Debugging a provider</span></span>

<span data-ttu-id="54f66-104">Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="54f66-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="54f66-105">À l'aide des commandes de débogage dans le composant de ruban de l'interface utilisateur Office Fluent dans Outlook ou de l'application cliente Office de prise en charge, la commande OSC doit prendre différentes actions.</span><span class="sxs-lookup"><span data-stu-id="54f66-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="54f66-106">En utilisant Fiddler pour suivre les appels d'API et le code XML envoyé entre un réseau social et son fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="54f66-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="54f66-107">Boutons de déBogage</span><span class="sxs-lookup"><span data-stu-id="54f66-107">Debug buttons</span></span>

<span data-ttu-id="54f66-108">L'extensibilité du fournisseur OSC permet de déboguer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="54f66-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="54f66-109">Pour déboguer un fournisseur, `DebugProviders` créez une valeur de type DWORD dans le Registre Windows `SocialConnector` sous la clé (comme indiqué dans la ligne suivante), et `DebugProviders` définissez la valeur sur 1.</span><span class="sxs-lookup"><span data-stu-id="54f66-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="54f66-110">Par défaut, le débogage du fournisseur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="54f66-110">By default, provider debugging is off.</span></span> <span data-ttu-id="54f66-111">Si la `DebugProviders` valeur n'est pas présente, ou si elle est présente et définie sur 0, le débogage du fournisseur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="54f66-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="54f66-112">Si le débogage du fournisseur est activé, le OSC affiche une boîte de dialogue d'alerte avec des informations détaillées sur l'erreur lorsqu'une erreur se produit et valide les fournisseurs OSC XML par rapport au schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="54f66-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="54f66-113">En fonction de l'espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l'aide de OSC 1,0 est validé par rapport au fichier de schéma OSC 1,0, OutlookSocialProvider. xsd.</span><span class="sxs-lookup"><span data-stu-id="54f66-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="54f66-114">Un fournisseur OSC développé à l'aide de OSC 1,1 ou version ultérieure est validé par rapport au fichier de schéma OutlookSocialProvider_ 1.1. xsd.</span><span class="sxs-lookup"><span data-stu-id="54f66-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="54f66-115">Lorsque vous utilisez la `DebugProviders` valeur, l'alerte de débogage apparaît pour tous les fournisseurs chargés au lieu d'un fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="54f66-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="54f66-116">Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez une `ShowDebugButtons` valeur de type DWORD `SocialConnector` dans le Registre Windows sous `ShowDebugButtons` la clé, et définissez la valeur sur 1.</span><span class="sxs-lookup"><span data-stu-id="54f66-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="54f66-117">Pour masquer les boutons de la barre de commandes de `ShowDebugButtons` débogage, définissez la valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="54f66-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="54f66-118">Pour Outlook 2010 et les applications clientes depuis Office 2013, les boutons de débogage apparaissent sous l'onglet **compléments** du ruban Explorateur.</span><span class="sxs-lookup"><span data-stu-id="54f66-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="54f66-119">Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent sur la barre de commandes standard de la fenêtre de l'explorateur Outlook.</span><span class="sxs-lookup"><span data-stu-id="54f66-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="54f66-120">Le tableau suivant décrit les boutons de débogage.</span><span class="sxs-lookup"><span data-stu-id="54f66-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="54f66-121">**Bouton déBogage**</span><span class="sxs-lookup"><span data-stu-id="54f66-121">**Debug button**</span></span>|<span data-ttu-id="54f66-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="54f66-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54f66-123">Synchroniser les contacts</span><span class="sxs-lookup"><span data-stu-id="54f66-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="54f66-124">Indique à l'OSC de demander au fournisseur OSC les contacts mis en cache uniquement.</span><span class="sxs-lookup"><span data-stu-id="54f66-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="54f66-125">Synchronisation de la liste d'adresses globale</span><span class="sxs-lookup"><span data-stu-id="54f66-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="54f66-126">Permet à OSC de remplir les données de la liste d'adresses globale d'Exchange vers les contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="54f66-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="54f66-127">Cache de catégorie Invalidate</span><span class="sxs-lookup"><span data-stu-id="54f66-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="54f66-128">La méthode OSC charge de nouveau la liste de catégories pour chaque banque lorsque le flux d'activités est actualisé.</span><span class="sxs-lookup"><span data-stu-id="54f66-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="54f66-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="54f66-129">Fiddler</span></span>

<span data-ttu-id="54f66-130">Fiddler est un outil de débogage par câble permettant de vérifier les appels d'API envoyés par votre fournisseur au réseau social, ainsi que le code XML envoyé par le réseau social à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="54f66-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="54f66-131">Fiddler peut être téléchargé sur le [proxy de débogage Web Fiddler](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="54f66-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54f66-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54f66-132">See also</span></span>

- [<span data-ttu-id="54f66-133">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="54f66-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="54f66-134">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="54f66-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="54f66-135">Meilleures pratiques pour le développement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="54f66-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="54f66-136">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="54f66-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="54f66-137">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="54f66-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="54f66-138">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="54f66-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

