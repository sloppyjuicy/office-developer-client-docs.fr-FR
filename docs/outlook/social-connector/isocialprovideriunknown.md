---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Représente une instance d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409957"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Représente une instance d’un fournisseur Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider.** 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Propriété  <br/> |Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Méthode  <br/> |Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Méthode  <br/> |Obtient une chaîne qui décrit les fonctionnalités du fournisseur.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialSession.](isocialsessioniunknown.md)  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Méthode  <br/> |Initialise le fournisseur OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Propriété  <br/> |Renvoie un GUID qui représente un identificateur unique pour le réseau social.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Propriété  <br/> |Renvoie un tableau d’octets qui représente l’icône du réseau social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente le nom du réseau social.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook Interfaces de fournisseur de connecteurs sociaux](outlook-social-connector-provider-interfaces.md)

