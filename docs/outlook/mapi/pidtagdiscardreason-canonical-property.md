---
title: Propriété canonique PidTagDiscardReason
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 32c81474580dbe4948c40390dadd0445776ab825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434801"
---
# <a name="pidtagdiscardreason-canonical-property"></a>Propriété canonique PidTagDiscardReason

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une raison pour laquelle un agent de transfert de messages (MTA) a ignoré un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISCARD_REASON  <br/> |
|Identificateur :  <br/> |0x0011  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La raison contenue dans cette propriété est utilisée dans un rapport de non-delivery pour le message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

