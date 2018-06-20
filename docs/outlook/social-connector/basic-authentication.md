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
# <a name="basic-authentication"></a>Authentification de base

L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. L’OSC utilise les capacités renvoyées pour déterminer comment prendre en charge d’un utilisateur d’Office qui se connecte à ce réseau social. Si l’élément **useLogonWebAuth** retournée **fonctionnalités** XML indique que le fournisseur OSC prend en charge l’authentification de base, l’OSC peut rendre la séquence d’appel suivante pour autoriser un utilisateur à se connecter à ce réseau social : 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — OSC la charge du fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — le OSC Obtient une chaîne qui représente le numéro de version du fournisseur OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — le OSC Obtient une chaîne qui représente le nom de réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — le OSC Obtient un GUID immuable qui représente le réseaux sociaux. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — le OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — le OSC Obtient un tableau d’octets qui représente l’icône pour le site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — le OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — le OSC connecte l’utilisateur au site de réseau social à l’aide du nom d’utilisateur et le mot de passe. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — le OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — le OSC Obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur de réseau peut être équivalente sur le nom de réseau. 
    
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

