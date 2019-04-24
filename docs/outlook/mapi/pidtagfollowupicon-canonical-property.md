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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316281"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propriété canonique PidTagFollowupIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la couleur de l'indicateur de l'objet message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificateur :  <br/> |0x1095  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Renommer le dossier de messages  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit exister que si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur «followupFlagged», ou l'objet message est un objet lié à la réunion. Cette propriété ne doit pas exister sur un objet Task. Lorsqu'elle est définie sur d'autres objets message, la valeur de cette propriété doit être l'une des valeurs suivantes.
  
|**Valeur numérique**|**Nom**|**Description**|
|:-----|:-----|:-----|
|Non présent  <br/> |S/O  <br/> |Aucune couleur  <br/> |
|0,1  <br/> |followupIcon1  <br/> |Drapeau violet  <br/> |
|n°2  <br/> |followupIcon2  <br/> |Drapeau Orange  <br/> |
|3  <br/> |followupIcon3  <br/> |Drapeau vert  <br/> |
|4  <br/> |followupIcon4  <br/> |Drapeau jaune  <br/> |
|disque  <br/> |followupIcon5  <br/> |Drapeau bleu  <br/> |
|6.x  <br/> |followupIcon6  <br/> |Drapeau rouge  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations relatives au marquage.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

