---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l'ajout de amis, la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345296"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Prend en charge l'ajout de amis, la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l'interface **ISocialSession2** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par les paramètres _EmailAddresses_ et _DisplayName_ comme un ami pour l'utilisateur connecté sur le réseau social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente une collection d'activités des utilisateurs spécifiés par le paramètre _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Méthode  <br/> |Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Méthode  <br/> |Ouvre une session sur le site réseau social en utilisant les informations d'identification mises en cache.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) peut choisir d'implémenter cette interface si le fournisseur prend en charge la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache. Si le fournisseur OSC implémente **ISocialSession2** et prend en charge les personnes suivantes sur le réseau social, le OSC appelle [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession:: followPerson](isocialsession-followperson.md), et le fournisseur doit implémenter **ISocialSession2:: FollowPersonEx**.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

