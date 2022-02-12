---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Représente une personne sur le réseau social.
ms.openlocfilehash: bcd507614da9ac9cb761f90bf801237ebefc23a7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774741"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Représente une personne sur le réseau social.
  
## <a name="members"></a>Members

Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialPerson** . 
  
|**Name**|**Type de membre**|**Description**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Méthode  <br/> |Cette méthode est dépréciée depuis Outlook Social Connector 2013. |
|[GetDetails](isocialperson-getdetails.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente les détails de la personne, tels que le prénom, le nom et l’URL d’une image de profil. |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Méthode  <br/> |Obtient une chaîne qui représente une collection de personnes. |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge. |
|[GetPicture](isocialperson-getpicture.md) <br/> |Méthode  <br/> |Obtient un tableau d’octets qui contient la ressource d’image de la personne. |
|[GetStatus](isocialperson-getstatus.md) <br/> |Méthode  <br/> |Cette méthode n’est actuellement pas prise en charge. |
   
## <a name="remarks"></a>Remarques

Un fournisseur Outlook Social Connector (OSC) doit implémenter cette interface pour communiquer avec OSC.
  
## <a name="see-also"></a>Voir aussi

- [Outlook interfaces de fournisseur Social Connector](outlook-social-connector-provider-interfaces.md)

