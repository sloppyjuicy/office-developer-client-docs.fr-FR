---
title: Authentification basée sur les formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Le Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435529"
---
# <a name="forms-based-authentication"></a>Authentification basée sur les formulaires

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. L’OSC utilise les fonctionnalités retournées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. 

Si l’élément **useLogonWebAuth** dans le **XML** des fonctionnalités renvoyées indique que le fournisseur OSC prend en charge l’authentification basée sur les formulaires, l’OSC peut effectuer la séquence d’appels suivante pour permettre à un utilisateur de se connecter à ce réseau social : 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; L’OSC charge le fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; L’OSC obtient une chaîne qui représente le numéro de version du fournisseur pour ce réseau social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; L’OSC obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; L’OSC obtient un GUID immuable qui représente le réseau social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; L’OSC obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma de **l’élément capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OsC obtient un tableau d’byte qui représente l’icône du site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; L’OSC obtient une interface [ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC initialise la connexion au site de réseau social à l’aide de l’authentification basée sur les formulaires. Pour cet appel de connexion initial, OSC transmet la valeur **null** pour le _paramètre connectIn._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OsC obtient l’URL pour afficher un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC termine l’accès au site de réseau social à l’aide de l’authentification basée sur les formulaires. L’OSC appelle cette méthode une deuxième fois, en passant l’URL du formulaire de connexion au fournisseur dans le _paramètre connectIn._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; L’OSC obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; L’OSC obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur réseau peut être équivalent au nom du réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

