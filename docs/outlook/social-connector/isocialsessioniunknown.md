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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357364"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Représente une connexion à un site de réseau social.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l'interface **ISocialSession** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente une ou plusieurs personnes qui correspondent au paramètre _userid_ .  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par le paramètre _EmailAddress_ en tant qu'ami pour l'utilisateur connecté sur le réseau social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Méthode  <br/> |Cette méthode a été déconseillée dans Outlook Social Connector (OSC) 1,1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialProfile](isocialprofileisocialperson.md) qui représente l'utilisateur connecté.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente un identificateur unique de réseau social pour une connexion de réseau social donnée.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Méthode  <br/> |Obtient une interface [ISocialPerson](isocialpersoniunknown.md) basée sur le paramètre _userid_ .  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Propriété  <br/> |Renvoie une chaîne qui représente l'ID d'utilisateur du réseau social de l'utilisateur actuellement connecté.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Propriété  <br/> |Renvoie une valeur de type String qui représente le nom d'utilisateur utilisé lors de l'ouverture de session.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Méthode  <br/> |Ouvre une session sur le site du réseau social en utilisant le nom d'utilisateur et le mot de passe spécifiés.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Méthode  <br/> |Ouvre une session sur le site réseau social à l'aide de l'authentification basée sur les formulaires.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Propriété  <br/> |Définit l'URL du site réseau social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Méthode  <br/> |Supprime la personne identifiée par le paramètre _userid_ en tant qu'ami sur le réseau social.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur OSC doit implémenter cette interface pour communiquer avec OSC.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

