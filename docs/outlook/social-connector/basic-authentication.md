---
title: Authentification de base
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439925"
---
# <a name="basic-authentication"></a><span data-ttu-id="2dc88-103">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="2dc88-103">Basic authentication</span></span>

<span data-ttu-id="2dc88-104">Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="2dc88-105">L’OSC utilise les fonctionnalités retournées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="2dc88-106">Si l’élément **useLogonWebAuth** dans le **XML** des fonctionnalités renvoyées indique que le fournisseur OSC prend en charge l’authentification de base, l’OSC peut effectuer la séquence d’appels suivante pour permettre à un utilisateur de se connecter à ce réseau social :</span><span class="sxs-lookup"><span data-stu-id="2dc88-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="2dc88-107">[ISocialProvider::Load :](isocialprovider-load.md) OSC charge le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2dc88-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="2dc88-108">[ISocialProvider::Version](isocialprovider-version.md) : l’OSC obtient une chaîne qui représente le numéro de version du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="2dc88-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="2dc88-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) : OSC obtient une chaîne qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="2dc88-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : OSC obtient un GUID immuable qui représente le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="2dc88-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) : l’OSC obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities.**</span><span class="sxs-lookup"><span data-stu-id="2dc88-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="2dc88-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) : OSC obtient un tableau d’byte qui représente l’icône du site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="2dc88-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) : OSC obtient une interface [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="2dc88-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="2dc88-114">[ISocialSession::Logon](isocialsession-logon.md) : OSC connecte l’utilisateur au site de réseau social à l’aide du nom d’utilisateur et du mot de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2dc88-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="2dc88-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : l’OSC obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="2dc88-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="2dc88-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) : OSC obtient une chaîne qui représente un identificateur unique pour un site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="2dc88-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="2dc88-117">L’identificateur réseau peut être équivalent au nom du réseau.</span><span class="sxs-lookup"><span data-stu-id="2dc88-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2dc88-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dc88-118">See also</span></span>

- [<span data-ttu-id="2dc88-119">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2dc88-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="2dc88-120">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="2dc88-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

