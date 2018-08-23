---
title: Propriété canonique PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c1b8c55a019ee3243de18d5e20ee4084bf6ca11f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581250"
---
# <a name="pidlidrecurring-canonical-property"></a>Propriété canonique PidLidRecurring

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique si un message d’un rendez-vous périodique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRecurring  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008223  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a la valeur TRUE si le rendez-vous est un rendez-vous périodique et a la valeur FALSE si elle n’est pas périodique.
  
Cette propriété spécifie si l’objet représente une série périodique. La valeur TRUE indique que l’objet représente une série périodique. La valeur FALSE, ou l’absence de cette propriété, indique que l’objet représente une instance unique ou une exception (y compris une instance orpheline). Notez la différence entre cette propriété et la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).
  
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

