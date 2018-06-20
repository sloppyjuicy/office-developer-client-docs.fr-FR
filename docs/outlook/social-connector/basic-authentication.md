---
title: Authentification de base
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: L’Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787601"
---
# <a name="basic-authentication"></a><span data-ttu-id="4ba44-103">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="4ba44-103">Basic authentication</span></span>

<span data-ttu-id="4ba44-104">L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="4ba44-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="4ba44-105">L’OSC utilise les capacités renvoyées pour déterminer comment prendre en charge d’un utilisateur d’Office qui se connecte à ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="4ba44-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="4ba44-106">Si l’élément **useLogonWebAuth** retournée **fonctionnalités** XML indique que le fournisseur OSC prend en charge l’authentification de base, l’OSC peut rendre la séquence d’appel suivante pour autoriser un utilisateur à se connecter à ce réseau social :</span><span class="sxs-lookup"><span data-stu-id="4ba44-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="4ba44-107">[ISocialProvider::Load](isocialprovider-load.md) — OSC la charge du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4ba44-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="4ba44-108">[ISocialProvider::Version](isocialprovider-version.md) — le OSC Obtient une chaîne qui représente le numéro de version du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="4ba44-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="4ba44-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — le OSC Obtient une chaîne qui représente le nom de réseau social.</span><span class="sxs-lookup"><span data-stu-id="4ba44-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="4ba44-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — le OSC Obtient un GUID immuable qui représente le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="4ba44-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="4ba44-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — le OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="4ba44-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="4ba44-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — le OSC Obtient un tableau d’octets qui représente l’icône pour le site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="4ba44-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="4ba44-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) — le OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba44-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="4ba44-114">[ISocialSession::Logon](isocialsession-logon.md) — le OSC connecte l’utilisateur au site de réseau social à l’aide du nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4ba44-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="4ba44-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — le OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="4ba44-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="4ba44-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — le OSC Obtient une chaîne qui représente un identificateur unique pour un site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="4ba44-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="4ba44-117">L’identificateur de réseau peut être équivalente sur le nom de réseau.</span><span class="sxs-lookup"><span data-stu-id="4ba44-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4ba44-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ba44-118">See also</span></span>

- [<span data-ttu-id="4ba44-119">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4ba44-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="4ba44-120">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="4ba44-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

