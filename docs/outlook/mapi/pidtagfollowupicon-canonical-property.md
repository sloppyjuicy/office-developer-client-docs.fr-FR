---
title: PidTagFollowupIcon Canonical, propriété
description: Décrit la propriété canonique PidTagFollowupIcon, qui spécifie la couleur d’indicateur de l’objet message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
ms.openlocfilehash: b141145c9539f639ce7ed281b8a7fa75a2eb88dd
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770977"
---
# <a name="pidtagfollowupicon-canonical-property"></a>PidTagFollowupIcon Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la couleur d’indicateur de l’objet message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificateur :  <br/> |0x1095  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Renommer le dossier de messages  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister, sauf si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur « followupFlagged » ou si l’objet message est un objet lié à la réunion. Cette propriété ne doit pas exister sur un objet de tâche. Lorsqu’elle est définie sur d’autres objets de message, cette propriété doit être définie sur l’une des valeurs suivantes.
  
|**Valeur numérique**|**Name**|**Description**|
|:-----|:-----|:-----|
|Non présent  <br/> |S/O  <br/> |Aucune couleur  <br/> |
|1  <br/> |followupIcon1  <br/> |Indicateur violet  <br/> |
|2  <br/> |followupIcon2  <br/> |Indicateur orange  <br/> |
|3  <br/> |followupIcon3  <br/> |Indicateur vert  <br/> |
|4  <br/> |followupIcon4  <br/> |Indicateur jaune  <br/> |
|5  <br/> |followupIcon5  <br/> |Indicateur bleu  <br/> |
|6   <br/> |followupIcon6  <br/> |Indicateur rouge  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

