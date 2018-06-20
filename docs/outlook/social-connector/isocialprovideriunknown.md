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
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787725"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Représente une instance d’un fournisseur Outlook Social Connector (OSC).
  
## <a name="members"></a>Membres

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Property  <br/> |Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Méthode  <br/> |Obtient une chaîne qui décrit les fonctionnalités du fournisseur.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Méthode  <br/> |Cette méthode n’est pas actuellement pris en charge.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Méthode  <br/> |Initialise le fournisseur OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Property  <br/> |Renvoie un GUID qui représente un identificateur unique pour le réseaux sociaux.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Property  <br/> |Renvoie un tableau d’octets qui représente l’icône du réseau social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le nom de réseau social.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le numéro de version du fournisseur de ce réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

