---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Représente une instance d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: b784ce945988c983d28d93fd351bb2d10b4e48ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583008"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Représente une instance d’un fournisseur Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider.** 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Property  <br/> |Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Méthode  <br/> |Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Méthode  <br/> |Obtient une chaîne qui décrit les fonctionnalités du fournisseur.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialSession.](isocialsessioniunknown.md)  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Méthode  <br/> |Initialise le fournisseur OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Property  <br/> |Renvoie un GUID qui représente un identificateur unique pour le réseau social.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Property  <br/> |Renvoie un tableau d’octets qui représente l’icône du réseau social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le nom du réseau social.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook Interfaces de fournisseur de connecteurs sociaux](outlook-social-connector-provider-interfaces.md)

