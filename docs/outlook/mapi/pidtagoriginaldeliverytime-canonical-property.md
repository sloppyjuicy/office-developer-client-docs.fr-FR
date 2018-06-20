---
title: Propriété canonique PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cd8c44923e64fcea4464f758389db05bb6b7e374
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786299"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a>Propriété canonique PidTagOriginalDeliveryTime

  
  
**S’applique à**: Outlook 
  
Contient une copie de la date de remise du message d’origine et l’heure dans un thread. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_DELIVERY_TIME  <br/> |
|Identificateur :  <br/> |0x0055  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est copiée à partir de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) d’origine dans la réponse suivante ou les opérations transférer et utilisée dans les rapports de lecture et nonread. Rapports de remise utilisent plutôt la propriété **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

