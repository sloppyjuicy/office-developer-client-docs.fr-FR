---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.
ms.openlocfilehash: a139f65b9761b088a41356940ec27959c6519764
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771803"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Prend en charge l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres disponibles sur l’interface **ISocialSession2** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par les paramètres  _emailAddresses_ et  _displayName_ en tant qu’ami de l’utilisateur connecté sur le réseau social. |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une collection d’activités des utilisateurs spécifiés par le paramètre  _hashedAddresses_ . |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Méthode  <br/> |Renvoie une chaîne qui contient une collection de détails de personne et d’image pour les utilisateurs spécifiés par le paramètre  _personsAddresses_ . |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Méthode  <br/> |Se connecte au site de réseau social à l’aide des informations d’identification mises en cache. |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) peut choisir d’implémenter cette interface si le fournisseur prend en charge la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache. Si le fournisseur OSC implémente **ISocialSession2** et prend en charge les personnes suivantes sur le réseau social, l’OSC appelle [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md), et le fournisseur doit également implémenter **ISocialSession2::FollowPersonEx**.
  
## <a name="see-also"></a>Voir aussi

- [Outlook interfaces de fournisseur Social Connector](outlook-social-connector-provider-interfaces.md)

