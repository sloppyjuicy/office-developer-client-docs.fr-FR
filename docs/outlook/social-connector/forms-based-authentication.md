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
# <a name="forms-based-authentication"></a>Authentification basée sur les formulaires

L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. L’OSC utilise les capacités renvoyées pour déterminer comment prendre en charge d’un utilisateur d’Office qui se connecte à ce réseau social. 

Si l’élément **useLogonWebAuth** retournée **fonctionnalités** XML indique que le fournisseur OSC prend en charge l’authentification basée sur les formulaires, l’OSC peut rendre la séquence d’appel suivante pour autoriser un utilisateur à se connecter à ce réseau social : 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC la charge du fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; L’OSC Obtient une chaîne qui représente le numéro de version du fournisseur de ce réseau social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; L’OSC Obtient une chaîne qui représente le nom de réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; L’OSC Obtient un GUID immuable qui représente le réseaux sociaux. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; L’OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l’élément **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; L’OSC Obtient un tableau d’octets qui représente l’icône pour le site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; L’OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC initialise se connecter au site de réseau social à l’authentification basée sur les formulaires. Pour que cet appel initial d’ouverture de session, l’OSC passe **null** pour le paramètre _connectIn_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; L’OSC Obtient l’URL pour afficher un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC la fin de la connexion au site de réseau social à l’aide de l’authentification basée sur les formulaires. L’OSC appelle cette méthode une deuxième fois, en passant l’URL du formulaire d’ouverture de session pour le fournisseur dans le paramètre _connectIn_ . 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; L’OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; L’OSC Obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur de réseau peut être équivalente sur le nom de réseau. 
    
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

