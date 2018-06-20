---
title: Propriété canonique PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785993"
---
# <a name="pidtagflagstatus-canonical-property"></a>Propriété canonique PidTagFlagStatus

  
  
**S’applique à**: Outlook 
  
Spécifie l’état de l’indicateur de l’objet du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FLAG_STATUS  <br/> |
|Identificateur :  <br/> |0x1090  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister sur un objet liées à la réunion, et il ne doit pas exister sur un objet task. Lorsque la valeur sur d’autres objets de message, vous devez définir cette propriété sur une des valeurs suivantes :
  
|**Valeur numérique**|**Nom**|**Description**|
|:-----|:-----|:-----|
|Absent  <br/> |S/O  <br/> |Sans indicateur  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Marqué comme terminé  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Marqué d’un indicateur  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
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

