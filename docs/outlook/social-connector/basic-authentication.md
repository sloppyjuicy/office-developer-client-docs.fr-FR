---
title: Authentification de base
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'Outlook Social Connector (OSC) appelle la méthode ISocialProvider:: GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281219"
---
# <a name="basic-authentication"></a><span data-ttu-id="6f569-103">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="6f569-103">Basic authentication</span></span>

<span data-ttu-id="6f569-104">Outlook Social Connector (OSC) appelle la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="6f569-105">Le OSC utilise les fonctionnalités renvoyées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="6f569-106">Si l'élément **useLogonWebAuth** dans le fichier XML de **fonctionnalités** renvoyé indique que le fournisseur OSC prend en charge l'authentification de base, le OSC peut effectuer la séquence d'appel suivante pour permettre à un utilisateur de se connecter à ce réseau social:</span><span class="sxs-lookup"><span data-stu-id="6f569-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="6f569-107">[ISocialProvider:: Load](isocialprovider-load.md) : OSC charge le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6f569-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="6f569-108">[ISocialProvider:: version](isocialprovider-version.md) — le OSC Obtient une chaîne qui représente le numéro de version du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="6f569-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="6f569-109">[ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) — le OSC Obtient une chaîne qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="6f569-110">[ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : le OSC Obtient un GUID non modifiable qui représente le réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="6f569-111">[ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) : le OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l'élément **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="6f569-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="6f569-112">[ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — le OSC Obtient un tableau d'octets qui représente l'icône du site du réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="6f569-113">[ISocialProvider:: GetSession](isocialprovider-getsession.md) — le OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6f569-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="6f569-114">[ISocialSession:: Logon](isocialsession-logon.md) — le OSC connecte l'utilisateur au site réseau social en utilisant le nom d'utilisateur et le mot de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6f569-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="6f569-115">[ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) — le OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="6f569-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="6f569-116">[ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — le OSC Obtient une chaîne qui représente un identificateur unique pour un site réseau social.</span><span class="sxs-lookup"><span data-stu-id="6f569-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="6f569-117">L'identificateur réseau peut être équivalent au nom réseau.</span><span class="sxs-lookup"><span data-stu-id="6f569-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6f569-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f569-118">See also</span></span>

- [<span data-ttu-id="6f569-119">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="6f569-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="6f569-120">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="6f569-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

