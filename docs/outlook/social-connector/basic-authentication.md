---
title: Authentification de base
description: Décrit la séquence d’appel que le Outlook Connecteur social peut effectuer pour permettre à un utilisateur de se connecter à un réseau social.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
ms.openlocfilehash: 1d54354666d48058c0da5f73e09ad1c3822014ac
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853096"
---
# <a name="basic-authentication"></a>Authentification de base

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Le système d’exploitation utilise les fonctionnalités retournées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. Si l’élément **useLogonWebAuth** dans le code XML **des fonctionnalités** retournées indique que le fournisseur OSC prend en charge l’authentification de base, l’OSC peut effectuer la séquence d’appels suivante pour permettre à un utilisateur de se connecter à ce réseau social : 
  
1. [ISocialProvider::Load](isocialprovider-load.md) : le système d’exploitation charge le fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) : l’OSC obtient une chaîne qui représente le numéro de version du fournisseur OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) : l’OSC obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : le OSC obtient un GUID immuable qui représente le réseau social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) : le osc obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma de l’élément **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) : l’OSC obtient un tableau d’octets qui représente l’icône du site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) : l’OSC obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::Logon](isocialsession-logon.md) : l’OSC connecte l’utilisateur au site de réseau social à l’aide du nom d’utilisateur et du mot de passe spécifiés. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : l’OSC obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) : l’OSC obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur réseau peut être équivalent au nom du réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

