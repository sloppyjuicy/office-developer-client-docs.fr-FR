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
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787627"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Représente une connexion à un site de réseau social.
  
## <a name="members"></a>Membres

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialSession** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au paramètre _userID_ .  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par le paramètre _emailAddress_ comme un ami pour l’utilisateur connecté sur le réseau social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Méthode  <br/> |Cette méthode a été désapprouvée dans Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialProfile](isocialprofileisocialperson.md) qui représente l’utilisateur connecté.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une URL qui est utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donné.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialPerson](isocialpersoniunknown.md) en fonction du paramètre _userID_ .  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente l’ID d’utilisateur de réseau social de l’utilisateur actuellement connecté.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Property  <br/> |Renvoie une chaîne qui représente le nom d’utilisateur qui est utilisé lors de la connexion.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Méthode  <br/> |Ouvre une session sur le site de réseau social à l’aide du nom d’utilisateur et le mot de passe.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Méthode  <br/> |Ouvre une session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Property  <br/> |Définit l’URL de site de réseau social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Méthode  <br/> |Supprime la personne identifiée par le paramètre _userID_ comme un ami sur le réseaux sociaux.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

