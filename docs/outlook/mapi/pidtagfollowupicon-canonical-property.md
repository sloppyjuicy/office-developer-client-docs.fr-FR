---
title: Propriété canonique PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593920"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propriété canonique PidTagFollowupIcon

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie la couleur de l’objet du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificateur :  <br/> |0x1095  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Renommer le dossier de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister, sauf si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur « followupFlagged » ou l’objet du message est un objet liées à la réunion. Cette propriété ne doit pas exister sur un objet task. Lorsque la valeur sur d’autres objets de message, cette propriété doit avoir une des valeurs suivantes.
  
|**Valeur numérique**|**Nom**|**Description**|
|:-----|:-----|:-----|
|Absent  <br/> |S/O  <br/> |Aucune couleur  <br/> |
|1  <br/> |followupIcon1  <br/> |Indicateur violet  <br/> |
|2  <br/> |followupIcon2  <br/> |Indicateur orange  <br/> |
|3  <br/> |followupIcon3  <br/> |Indicateur vert  <br/> |
|4  <br/> |followupIcon4  <br/> |Indicateur jaune  <br/> |
|5  <br/> |followupIcon5  <br/> |Indicateur bleu  <br/> |
|6  <br/> |followupIcon6  <br/> |Indicateur rouge  <br/> |
   
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

