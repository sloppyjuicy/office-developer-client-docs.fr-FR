---
title: Authentification basée sur les formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: L’Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787589"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="dbb15-103">Authentification basée sur les formulaires</span><span class="sxs-lookup"><span data-stu-id="dbb15-103">Forms-based authentication</span></span>

<span data-ttu-id="dbb15-104">L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="dbb15-105">L’OSC utilise les capacités renvoyées pour déterminer comment prendre en charge d’un utilisateur d’Office qui se connecte à ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="dbb15-106">Si l’élément **useLogonWebAuth** retournée **fonctionnalités** XML indique que le fournisseur OSC prend en charge l’authentification basée sur les formulaires, l’OSC peut rendre la séquence d’appel suivante pour autoriser un utilisateur à se connecter à ce réseau social :</span><span class="sxs-lookup"><span data-stu-id="dbb15-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="dbb15-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC la charge du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dbb15-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="dbb15-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; L’OSC Obtient une chaîne qui représente le numéro de version du fournisseur de ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="dbb15-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; L’OSC Obtient une chaîne qui représente le nom de réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="dbb15-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; L’OSC Obtient un GUID immuable qui représente le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="dbb15-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="dbb15-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; L’OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="dbb15-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="dbb15-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; L’OSC Obtient un tableau d’octets qui représente l’icône pour le site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="dbb15-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; L’OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="dbb15-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="dbb15-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC initialise se connecter au site de réseau social à l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="dbb15-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="dbb15-115">Pour que cet appel initial d’ouverture de session, l’OSC passe **null** pour le paramètre _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="dbb15-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="dbb15-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; L’OSC Obtient l’URL pour afficher un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.</span><span class="sxs-lookup"><span data-stu-id="dbb15-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="dbb15-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC la fin de la connexion au site de réseau social à l’aide de l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="dbb15-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="dbb15-118">L’OSC appelle cette méthode une deuxième fois, en passant l’URL du formulaire d’ouverture de session pour le fournisseur dans le paramètre _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="dbb15-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="dbb15-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; L’OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="dbb15-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="dbb15-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; L’OSC Obtient une chaîne qui représente un identificateur unique pour un site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="dbb15-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="dbb15-121">L’identificateur de réseau peut être équivalente sur le nom de réseau.</span><span class="sxs-lookup"><span data-stu-id="dbb15-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dbb15-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb15-122">See also</span></span>

- [<span data-ttu-id="dbb15-123">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="dbb15-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="dbb15-124">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="dbb15-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

