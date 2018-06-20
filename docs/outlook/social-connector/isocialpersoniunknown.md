---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Représente une personne sur le réseau social.
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787596"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Représente une personne sur le réseau social.
  
## <a name="members"></a>Membres

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialPerson** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Méthode  <br/> |Cette méthode a été déconseillée depuis Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente les détails de la personne, telles que le prénom, nom et une URL vers une image de profil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une collection de personnes.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Méthode  <br/> |Cette méthode n’est pas actuellement pris en charge.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Méthode  <br/> |Obtient un tableau d’octets qui contient la ressource image de la personne.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Méthode  <br/> |Cette méthode n’est pas actuellement pris en charge.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) doit implémenter cette interface pour communiquer avec l’OSC.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

