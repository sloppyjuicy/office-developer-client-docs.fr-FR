---
title: Authentification de base
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Le Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 803fe6ae37bb408f8e3082e184317c4d19831906
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616256"
---
# <a name="basic-authentication"></a>Authentification de base

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. L’OSC utilise les fonctionnalités retournées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. Si l’élément **useLogonWebAuth** dans le **XML** des fonctionnalités renvoyées indique que le fournisseur OSC prend en charge l’authentification de base, l’OSC peut effectuer la séquence d’appels suivante pour permettre à un utilisateur de se connecter à ce réseau social : 
  
1. [ISocialProvider::Load :](isocialprovider-load.md) OSC charge le fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) : l’OSC obtient une chaîne qui représente le numéro de version du fournisseur OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) : OSC obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : OSC obtient un GUID immuable qui représente le réseau social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) : OSC obtient un tableau d’byte qui représente l’icône du site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) : OSC obtient une interface [ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::Logon](isocialsession-logon.md) : OSC connecte l’utilisateur au site de réseau social à l’aide du nom d’utilisateur et du mot de passe spécifiés. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : l’OSC obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) : OSC obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur réseau peut être équivalent au nom du réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

