---
title: Meilleures pratiques pour le développement d’un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur 2013 Outlook Social Connector (OSC) :'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787573"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="b51db-103">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b51db-103">Best practices for developing a provider</span></span>

<span data-ttu-id="b51db-104">Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur 2013 Outlook Social Connector (OSC) :</span><span class="sxs-lookup"><span data-stu-id="b51db-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="b51db-105">Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs via Internet doivent utiliser le protocole HTTPS (Hypertext Transfer Protocol (HTTP) avec Secure Socket Layer (SSL)).</span><span class="sxs-lookup"><span data-stu-id="b51db-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="b51db-106">Dans le cas contraire, il existe un risque que les adresses de messagerie, les activités de réseaux sociaux et autres utilisateur données peuvent être interceptées ou exposées lors de leur transit.</span><span class="sxs-lookup"><span data-stu-id="b51db-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="b51db-107">Si vous développez un fournisseur OSC pour un réseau social tiers, votre fournisseur doit respecter les conditions du réseau social de service.</span><span class="sxs-lookup"><span data-stu-id="b51db-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="b51db-108">Pour réduire la taille du package de téléchargement du fournisseur, créez le fournisseur à l’aide d’un compilateur natif tel que C++ ou tout autre outil qui peut créer un composant COM.</span><span class="sxs-lookup"><span data-stu-id="b51db-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="b51db-109">Dans votre fournisseur, créez un agent utilisateur unique qui est envoyé au réseau social pour effectuer le suivi des appels effectués par le fournisseur pour le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="b51db-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="b51db-110">La méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) doit s’appuie pas sur le réseaux sociaux d’appel via Internet pour obtenir les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b51db-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="b51db-111">Par exemple, les utilisateurs peuvent démarrer Outlook en mode hors connexion ; Si l’OSC appelle **GetCapabilities** et il n’existe pas de connexion réseau, l’appel **GetCapabilities** ne renvoie pas valide XML des **capacités** .</span><span class="sxs-lookup"><span data-stu-id="b51db-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="b51db-112">La meilleure pratique consiste à stocker les **fonctionnalités** XML en tant que ressource dans votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b51db-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="b51db-113">Votre fournisseur OSC peut générer un volume important d’appels à un réseau social.</span><span class="sxs-lookup"><span data-stu-id="b51db-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="b51db-114">Selon les termes du contrat de service pour votre réseau social, tenez compte des amis dans un dossier Outlook afin de réduire le nombre d’appels à partir de l’OSC à votre fournisseur et, à son tour, à partir de votre fournisseur de réseau social de la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="b51db-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="b51db-115">Office 2013 est disponible dans les versions 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b51db-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="b51db-116">Les versions d’Office avant d’Office 2010 sont disponibles uniquement dans une version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b51db-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="b51db-117">L’installation par défaut d’Office 2013 sur un ordinateur Windows 64 bits est de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b51db-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="b51db-118">Si vous souhaitez prendre en charge la version 64 bits de l’OSC qui est installé avec Office 2013 de 64 bits, vous devez également libérer une version 64 bits de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b51db-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b51db-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b51db-119">See also</span></span>

- [<span data-ttu-id="b51db-120">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="b51db-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="b51db-121">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="b51db-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="b51db-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b51db-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b51db-123">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b51db-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

