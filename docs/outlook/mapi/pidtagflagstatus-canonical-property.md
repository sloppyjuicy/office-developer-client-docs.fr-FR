---
title: Propriété canonique PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9793115f67c5c889d8c674e0279516177aac837a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616438"
---
# <a name="pidtagflagstatus-canonical-property"></a>Propriété canonique PidTagFlagStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’état d’indicateur de l’objet message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FLAG_STATUS  <br/> |
|Identificateur :  <br/> |0x1090  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister sur un objet lié à la réunion et elle ne doit pas exister sur un objet de tâche. Lorsqu’elle est définie sur d’autres objets de message, cette propriété doit être définie sur l’une des valeurs suivantes :
  
|**Valeur numérique**|**Name**|**Description**|
|:-----|:-----|:-----|
|Non présent  <br/> |N/A  <br/> |Non survolé  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Marqué comme terminé  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Marqué d’un indicateur  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

