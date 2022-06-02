---
title: Authentification basée sur les formulaires
description: Décrit la séquence d’appel que le Outlook Connecteur social peut effectuer pour permettre à un utilisateur de se connecter au réseau social.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
ms.openlocfilehash: 6ebb4403436b33fdcc0c150068d9432506143a80
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853908"
---
# <a name="forms-based-authentication"></a>Authentification basée sur les formulaires

Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Le système d’exploitation utilise les fonctionnalités retournées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. 

Si l’élément **useLogonWebAuth** dans le code XML **des fonctionnalités** retournées indique que le fournisseur OSC prend en charge l’authentification basée sur les formulaires, l’OSC peut effectuer la séquence d’appels suivante pour permettre à un utilisateur de se connecter à ce réseau social : 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; Le système d’exploitation charge le fournisseur. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; L’OSC obtient une chaîne qui représente le numéro de version du fournisseur pour ce réseau social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; L’OSC obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; L’OSC obtient un GUID immuable qui représente le réseau social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; L’OSC obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma de l’élément **de fonctionnalités** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; L’OSC obtient un tableau d’octets qui représente l’icône du site de réseau social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; L’OSC obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC initialise la connexion au site de réseau social par authentification basée sur les formulaires. Pour cet appel d’ouverture de session initial, l’OSC passe **la valeur null** pour le paramètre  _connectIn_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Le système d’exploitation obtient l’URL permettant d’afficher un formulaire basé sur un navigateur à l’utilisateur pendant l’authentification web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; L’OSC termine l’ouverture de session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires. Le système d’exploitation appelle cette méthode une deuxième fois, en passant l’URL du formulaire d’ouverture de session au fournisseur dans le paramètre _connectIn_ . 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; L’OSC obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l’utilisateur connecté. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; L’OSC obtient une chaîne qui représente un identificateur unique pour un site de réseau social. L’identificateur réseau peut être équivalent au nom du réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

