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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785907"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propriété canonique PidTagCorrelate

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si l’expéditeur d’un message de demande de la fonctionnalité de corrélation du système de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE  <br/> |
|Identificateur :  <br/> |0x0E0C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Exchange  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

