---
title: Propriété canonique PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785507"
---
# <a name="pidlidtimezone-canonical-property"></a>Propriété canonique PidLidTimeZone

  
  
**S’applique à**: Outlook 
  
Spécifie des informations sur le fuseau horaire d’une réunion périodique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |LID_TIME_ZONE  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID de type long (capot) :  <br/> |0x0000000C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est en lecture uniquement si la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) n’est pas définie, mais si la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) est TRUE et la **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) la propriété est FALSE. Le mot de poids faible spécifie un index dans un tableau qui contient des informations de fuseau horaire. À partir du mot supérieur, uniquement le bit le plus élevé est en lecture. Si ce bit est activé, puis le fuseau horaire référencé n’observera est suivi de l’heure (heure), sinon les dates de l’heure d’été détaillées dans [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

