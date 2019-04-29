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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439925"
---
# <a name="basic-authentication"></a>Authentification de base

Outlook Social Connector (OSC) appelle la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Le OSC utilise les fonctionnalités renvoyées pour déterminer comment prendre en charge un utilisateur Office qui se connecte à ce réseau social. Si l'élément **useLogonWebAuth** dans le fichier XML de **fonctionnalités** renvoyé indique que le fournisseur OSC prend en charge l'authentification de base, le OSC peut effectuer la séquence d'appel suivante pour permettre à un utilisateur de se connecter à ce réseau social: 
  
1. [ISocialProvider:: Load](isocialprovider-load.md) : OSC charge le fournisseur. 
    
2. [ISocialProvider:: version](isocialprovider-version.md) — le OSC Obtient une chaîne qui représente le numéro de version du fournisseur OSC. 
    
3. [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) — le OSC Obtient une chaîne qui représente le nom du réseau social. 
    
4. [ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : le OSC Obtient un GUID non modifiable qui représente le réseau social. 
    
5. [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) : le OSC Obtient une chaîne qui représente les fonctionnalités du fournisseur et qui est conforme à la définition de schéma pour l'élément **Capabilities** . 
    
6. [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — le OSC Obtient un tableau d'octets qui représente l'icône du site du réseau social. 
    
7. [ISocialProvider:: GetSession](isocialprovider-getsession.md) — le OSC Obtient une interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession:: Logon](isocialsession-logon.md) — le OSC connecte l'utilisateur au site réseau social en utilisant le nom d'utilisateur et le mot de passe spécifiés. 
    
9. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) — le OSC Obtient une interface [ISocialProfile](isocialprovideriunknown.md) qui représente l'utilisateur connecté. 
    
10. [ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — le OSC Obtient une chaîne qui représente un identificateur unique pour un site réseau social. L'identificateur réseau peut être équivalent au nom réseau. 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

