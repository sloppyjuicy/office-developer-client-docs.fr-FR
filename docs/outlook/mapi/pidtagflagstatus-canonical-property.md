---
title: PidTagFlagStatus, propriété canonique
description: Décrit la propriété canonique PidTagFlagStatus, qui spécifie l’état d’indicateur de l’objet message.
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
ms.openlocfilehash: 83e5d784cc043bde420eca820986b68dc8704eb3
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770697"
---
# <a name="pidtagflagstatus-canonical-property"></a>PidTagFlagStatus, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’état d’indicateur de l’objet message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FLAG_STATUS  <br/> |
|Identificateur :  <br/> |0x1090  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas exister sur un objet lié à une réunion et n’existe pas sur un objet de tâche. Lorsqu’elle est définie sur d’autres objets de message, cette propriété doit être définie sur l’une des valeurs suivantes :
  
|**Valeur numérique**|**Name**|**Description**|
|:-----|:-----|:-----|
|Non présent  <br/> |S/O  <br/> |Sans balises  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Marqué comme terminé  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Marqué d’un indicateur  <br/> |
   
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

