---
title: Propriété canonique PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405218"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propriété canonique PidTagCorrelate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si l'expéditeur d'un message demande la fonctionnalité de corrélation du système de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE  <br/> |
|Identificateur :  <br/> |0x0E0C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour demander la corrélation des rapports entrants avec le message d'origine envoyé. Lorsqu'un fournisseur de transport rencontre un message envoyé avec **PR_CORRELATE** défini sur true, il définit la propriété **PR_CORRELATE_MTSID** ([PIDTAGCORRELATEMTSID](pidtagcorrelatemtsid-canonical-property.md)) sur l'identificateur MTS (Message Transfer System) pour ce message.
  
 **PR_CORRELATE** doit être utilisé avec les systèmes de messagerie qui prennent en charge la corrélation par identificateur MTS, tel que X. 400. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

