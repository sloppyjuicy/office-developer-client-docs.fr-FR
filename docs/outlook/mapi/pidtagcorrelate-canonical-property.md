---
title: Propriété canonique PidTagCorrelate
description: Décrit la propriété canonique PidTagCorrelate, qui est utilisée pour demander la corrélation des rapports entrants avec le message envoyé d’origine.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
ms.openlocfilehash: 7d92ca78b05599297e6023d068e80ed85d3a6cda
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769752"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propriété canonique PidTagCorrelate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si l’expéditeur d’un message demande la fonctionnalité de corrélation du système de messagerie.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE  <br/> |
|Identificateur :  <br/> |0x0E0C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour demander la corrélation des rapports entrants avec le message envoyé d’origine. Lorsqu’un fournisseur de transport rencontre un message envoyé avec **PR_CORRELATE** défini sur TRUE, il définit la propriété **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) sur l’identificateur du système de transfert de messages (MTS) pour ce message.
  
 **PR_CORRELATE** doit être utilisé avec les systèmes de messagerie qui prennent en charge la corrélation par identificateur MTS, tel que X.400. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

