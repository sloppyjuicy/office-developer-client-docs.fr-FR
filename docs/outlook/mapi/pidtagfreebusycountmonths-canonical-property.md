---
title: Propriété canonique PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e7dc8c06fca48c5f7c124a1fdf2228ebeb9da450
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569980"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a>Propriété canonique PidTagFreeBusyCountMonths

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur pour calculer les dates de début et de fin de la plage de données et de disponibilité pour être publiés dans les dossiers publics.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FREEBUSY_COUNT_MONTHS  <br/> |
|Identificateur :  <br/> |0x6869  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Message défini par la classe transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Valeur de cette propriété doit être supérieure ou égale à 0 et inférieure ou égale à 36. Il n’est pas une propriété requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou une ressource.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

