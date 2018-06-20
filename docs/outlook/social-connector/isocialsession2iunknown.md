---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l’ajout de contacts, de synchronisation à la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787622"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Prend en charge l’ajout de contacts, de synchronisation à la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.
  
## <a name="members"></a>Membres

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialSession2** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Méthode  <br/> |Ajoute la personne identifiée par les paramètres _emailAddresses_ et _displayName_ comme un ami pour l’utilisateur connecté sur le réseau social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une collection d’activités des utilisateurs spécifiés par le paramètre _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Méthode  <br/> |Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Méthode  <br/> |Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) peut choisir d’implémenter cette interface si le fournisseur prend en charge la synchronisation de la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide des informations d’identification mises en cache. Si le fournisseur OSC implémente **ISocialSession2** et prend en charge de suivi de personnes sur le réseaux sociaux, le OSC appellent [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md), et le fournisseur doit implémenter **ISocialSession2::FollowPersonEx**, également.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

