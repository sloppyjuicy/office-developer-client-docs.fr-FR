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
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316295"
---
# <a name="pidtagflagstatus-canonical-property"></a>Propriété canonique PidTagFlagStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l'état de l'indicateur de l'objet message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FLAG_STATUS  <br/> |
|Identificateur :  <br/> |0x1090  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister sur un objet lié à une réunion et elle ne doit pas exister sur un objet Task. Lorsqu'elle est définie sur d'autres objets message, la valeur de cette propriété doit être l'une des valeurs suivantes:
  
|**Valeur numérique**|**Nom**|**Description**|
|:-----|:-----|:-----|
|Non présent  <br/> |S/O  <br/> |Unindicateur  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Indicateur complet  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Marqué d’un indicateur  <br/> |
   
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

