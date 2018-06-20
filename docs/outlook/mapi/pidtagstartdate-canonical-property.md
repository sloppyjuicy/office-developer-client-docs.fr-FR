---
title: Propriété canonique PidTagStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 14a077dfdb0f0781ab0d9f085c758c7a7d6285af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786824"
---
# <a name="pidtagstartdate-canonical-property"></a>Propriété canonique PidTagStartDate

  
  
**S’applique à**: Outlook 
  
Contient la date et l’heure d’un rendez-vous comme gérés par une application de planification départ.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_START_DATE  <br/> |
|Identificateur :  <br/> |0x0060  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Applications de planification doivent définir cette propriété et les propriétés **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) lors de l’envoi de demandes de réunion.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

