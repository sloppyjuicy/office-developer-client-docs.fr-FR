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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331940"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Représente une personne sur le réseau social.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l'interface **ISocialPerson** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Méthode  <br/> |Cette méthode a été déconseillée depuis Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente les détails de la personne, tels que le prénom, le nom et l'URL d'une image de profil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Méthode  <br/> |Obtient une valeur de type String qui représente une collection de personnes.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Méthode  <br/> |Cette méthode n'est pas prise en charge actuellement.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Méthode  <br/> |Obtient un tableau d'octets qui contient la ressource image de la personne.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Méthode  <br/> |Cette méthode n'est pas prise en charge actuellement.  <br/> |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) doit implémenter cette interface pour communiquer avec OSC.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fournisseur Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

