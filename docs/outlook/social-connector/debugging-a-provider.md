---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC) :'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281068"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="8a9a0-103">Débogage d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="8a9a0-103">Debugging a provider</span></span>

<span data-ttu-id="8a9a0-104">Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC) :</span><span class="sxs-lookup"><span data-stu-id="8a9a0-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="8a9a0-105">À l’aide des commandes de débogage dans le composant ruban de l’interface utilisateur Office Fluent dans Outlook ou de l’application cliente Office de prise en charge pour que l’OSC prenne différentes mesures.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="8a9a0-106">Utilisation de Fiddler pour suivre les appels d’API et le XML envoyés entre un réseau social et son fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="8a9a0-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="8a9a0-107">Boutons de débogage</span><span class="sxs-lookup"><span data-stu-id="8a9a0-107">Debug buttons</span></span>

<span data-ttu-id="8a9a0-108">L’extensibilité du fournisseur OSC permet de déboguer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="8a9a0-109">Pour déboguer un fournisseur, créez une valeur de type DWORD dans le Registre Windows sous la clé (comme illustré dans la ligne suivante) et définissez la valeur sur `DebugProviders` `SocialConnector` `DebugProviders` 1.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="8a9a0-110">Par défaut, le débogage du fournisseur est hors service.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-110">By default, provider debugging is off.</span></span> <span data-ttu-id="8a9a0-111">Si la valeur n’est pas présente, ou si elle est présente et définie sur la valeur 0, le débogage du fournisseur  `DebugProviders` est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="8a9a0-112">Si le débogage du fournisseur est allumé, l’OSC affiche une boîte de dialogue d’alerte avec des informations détaillées sur les erreurs lorsqu’une erreur se produit et valide tout XML de fournisseur OSC par rapport au schéma XML du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="8a9a0-113">En fonction de l’espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l’aide d’OSC 1.0 est validé par rapport au fichier de schéma OSC 1.0, OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="8a9a0-114">Un fournisseur OSC développé à l’aide d’OSC 1.1 ou ultérieur est validé par rapport au fichier de schéma, OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="8a9a0-115">Lorsque vous utilisez la valeur, l’alerte de débogage s’affiche pour tous les fournisseurs chargés au lieu  `DebugProviders` d’un fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="8a9a0-116">Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez une valeur de type DWORD dans le Registre Windows sous la clé et définissez la valeur sur `ShowDebugButtons` `SocialConnector` `ShowDebugButtons` 1.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="8a9a0-117">Pour masquer les boutons de barre de commandes de débogage, définissez  `ShowDebugButtons` la valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="8a9a0-118">Pour Outlook 2010 et les applications clientes depuis Office 2013, les  boutons de débogage apparaissent sous l’onglet Des applications du ruban de l’explorateur.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="8a9a0-119">Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent dans la barre de commandes standard de la fenêtre Outlook’explorateur.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="8a9a0-120">Le tableau suivant décrit les boutons de débogage.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="8a9a0-121">**Bouton Déboguer**</span><span class="sxs-lookup"><span data-stu-id="8a9a0-121">**Debug button**</span></span>|<span data-ttu-id="8a9a0-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8a9a0-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a9a0-123">Synchroniser les contacts</span><span class="sxs-lookup"><span data-stu-id="8a9a0-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="8a9a0-124">Fait que l’OSC demande uniquement au fournisseur OSC les contacts mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="8a9a0-125">Synchronisation de laxisme</span><span class="sxs-lookup"><span data-stu-id="8a9a0-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="8a9a0-126">Indique à OSC de remplir les données de la Exchange d’adresses globale pour Outlook contacts.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="8a9a0-127">Invalider le cache de catégories</span><span class="sxs-lookup"><span data-stu-id="8a9a0-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="8a9a0-128">Entraîne le rechargement par OSC de la liste des catégories pour chaque magasin lors de l’actualisation du flux d’activités.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="8a9a0-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="8a9a0-129">Fiddler</span></span>

<span data-ttu-id="8a9a0-130">Fiddler est un outil de débogage over-the-wire pour vérifier les appels d’API envoyés par votre fournisseur au réseau social et le XML envoyé par le réseau social à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8a9a0-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="8a9a0-131">Fiddler est disponible en téléchargement sur [fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="8a9a0-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a9a0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a9a0-132">See also</span></span>

- [<span data-ttu-id="8a9a0-133">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="8a9a0-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="8a9a0-134">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="8a9a0-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="8a9a0-135">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="8a9a0-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="8a9a0-136">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="8a9a0-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="8a9a0-137">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="8a9a0-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="8a9a0-138">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="8a9a0-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

