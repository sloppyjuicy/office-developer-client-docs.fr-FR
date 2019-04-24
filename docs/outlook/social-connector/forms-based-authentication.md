---
title: Authentification basée sur les formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'Outlook Social Connector (OSC) appelle la méthode ISocialProvider:: GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280989"
---
# <a name="forms-based-authentication"></a>Authentification basée sur les formulaires

Outlook Social Connector (OSC) appelle la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Le OSC utilise les fonctionnalités renvoyées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. 

Si l'élément **useLogonWebAuth** dans le fichier XML de **fonctionnalités** renvoyé indique que le fournisseur OSC prend en charge l'authentification basée sur les formulaires, le OSC peut effectuer la séquence d'appel suivante pour permettre à un utilisateur de se connecter à ce réseau social: 
  
1. [ISocialProvider:: Load](isocialprovider-load.md) &ndash; L'OSC charge le fournisseur. 
    
2. [ISocialProvider:: version](isocialprovider-version.md) &ndash; L'OSC Obtient une chaîne qui représente le numéro de version du fournisseur pour ce réseau social. 
    
3. [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; L'OSC Obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; L'interface OSC Obtient un GUID non modifiable qui représente le réseau social. 
    
5. [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) &ndash; Le OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l'élément **Capabilities** . 
    
6. [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; L'OSC Obtient un tableau d'octets qui représente l'icône du site du réseau social. 
    
7. [ISocialProvider:: GetSession](isocialprovider-getsession.md) &ndash; Le OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; L'OSC initialise la connexion au site réseau social via l'authentification basée sur les formulaires. Pour cet appel d'ouverture de session initial, OSC transmet **null** pour le paramètre _Connect_ . 
    
9. [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Le OSC Obtient l'URL pour afficher un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web. 
    
10. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; Le OSC termine la connexion au site réseau social à l'aide de l'authentification basée sur les formulaires. Le OSC appelle cette méthode une deuxième fois, en transmettant l'URL du formulaire de connexion au fournisseur dans le paramètre _Connect_ . 
    
11. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Le OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l'utilisateur connecté. 
    
12. [ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Le OSC Obtient une chaîne qui représente un identificateur unique pour un site réseau social. L'identificateur réseau peut être équivalent au nom réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

