---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Représente une connexion à un site de réseau social.
ms.openlocfilehash: 7efe8922f7f4dfa3c9cf06a910266c0d3bf2cdda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629066"
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
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente l’ID d’utilisateur du réseau social de l’utilisateur actuellement connecté.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le nom d’utilisateur utilisé lors de la connexion.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Méthode  <br/> |Se connecte au site de réseau social à l’aide du nom d’utilisateur et du mot de passe spécifiés.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Méthode  <br/> |Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Property  <br/> |Définit l’URL du site de réseau social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Méthode  <br/> |Supprime la personne identifiée par le paramètre  _userID_ en tant qu’ami sur le réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook Interfaces de fournisseur de connecteurs sociaux](outlook-social-connector-provider-interfaces.md)

