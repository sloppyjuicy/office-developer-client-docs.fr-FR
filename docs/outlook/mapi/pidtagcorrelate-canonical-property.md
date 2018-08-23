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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575454"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propriété canonique PidTagCorrelate

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si l’expéditeur d’un message de demande de la fonctionnalité de corrélation du système de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE  <br/> |
|Identificateur :  <br/> |0x0E0C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour demander la corrélation de rapports entrants avec le message d’origine envoyé. Lorsqu’un fournisseur de transport rencontre un message envoyé avec set **PR_CORRELATE** sur TRUE, il définit la propriété **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) à l’identificateur de système (MTS) de transfert de message pour le message.
  
 **PR_CORRELATE** doit être utilisé avec les systèmes qui prennent en charge la corrélation de messagerie par identificateur MTS, tels que X.400. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

