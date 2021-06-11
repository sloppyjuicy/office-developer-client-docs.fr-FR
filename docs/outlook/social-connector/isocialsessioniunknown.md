---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Représente une connexion à un site de réseau social.
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437825"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Représente une connexion à un site de réseau social.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialSession.** 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au _paramètre userID._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par le  _paramètre emailAddress_ en tant qu’ami de l’utilisateur connecté sur le réseau social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Méthode  <br/> |Cette méthode a été Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialProfile](isocialprofileisocialperson.md) qui représente l’utilisateur connecté.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur pendant l’authentification web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donnée.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialPerson](isocialpersoniunknown.md) basée sur le _paramètre userID._  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente l’ID d’utilisateur du réseau social de l’utilisateur actuellement connecté.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente le nom d’utilisateur utilisé lors de la connexion.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Méthode  <br/> |Se connecte au site de réseau social à l’aide du nom d’utilisateur et du mot de passe spécifiés.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Méthode  <br/> |Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Propriété  <br/> |Définit l’URL du site de réseau social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Méthode  <br/> |Supprime la personne identifiée par le  _paramètre userID_ en tant qu’ami sur le réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook Interfaces de fournisseur de connecteurs sociaux](outlook-social-connector-provider-interfaces.md)

