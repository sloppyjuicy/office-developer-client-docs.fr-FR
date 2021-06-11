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
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407010"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Représente une personne sur le réseau social.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres disponibles sur l’interface **ISocialPerson.** 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Méthode  <br/> |Cette méthode est dépréciée depuis Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente les détails de la personne, tels que le prénom, le nom et l’URL d’une image de profil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une collection de personnes.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Méthode  <br/> |Obtient un tableau d’octets qui contient la ressource d’image de la personne.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) doit implémenter cette interface pour communiquer avec OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook Interfaces de fournisseur de connecteurs sociaux](outlook-social-connector-provider-interfaces.md)

