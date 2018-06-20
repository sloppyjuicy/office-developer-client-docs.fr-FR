---
title: Propriété canonique PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786372"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Propriété canonique PidTagOriginatorDeliveryReportRequested

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un expéditeur du message demande un rapport de remise pour un destinataire à partir du système de messagerie particulier avant que le message est placé dans la banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0023  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages remis. Dans ce cas, le message doit fournir également la propriété **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) la valeur FALSE.
  
La propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** d’un message est un moyen de demander des rapports d’état de remise pour tous les destinataires. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
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

