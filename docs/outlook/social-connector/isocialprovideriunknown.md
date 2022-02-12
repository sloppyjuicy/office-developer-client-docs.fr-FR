---
title: ISocialProvider  IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Représente une instance d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 571eea9978e5a97255910bb805164039ccc43a02
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770646"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Représente une instance d’un fournisseur Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Propriété  <br/> |Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC. |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Méthode  <br/> |Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement. |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Méthode  <br/> |Obtient une chaîne qui décrit les fonctionnalités du fournisseur. |
|[GetSession](isocialprovider-getsession.md) <br/> |Méthode  <br/> |Obtient [une interface ISocialSession](isocialsessioniunknown.md) . |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge. |
|[Load](isocialprovider-load.md) <br/> |Méthode  <br/> |Initialise le fournisseur OSC. |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Propriété  <br/> |Renvoie un GUID qui représente un identificateur unique pour le réseau social. |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Propriété  <br/> |Renvoie un tableau d’octets qui représente l’icône du réseau social. |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente le nom du réseau social. |
|[Version](isocialprovider-version.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social. |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook interfaces de fournisseur Social Connector](outlook-social-connector-provider-interfaces.md)

