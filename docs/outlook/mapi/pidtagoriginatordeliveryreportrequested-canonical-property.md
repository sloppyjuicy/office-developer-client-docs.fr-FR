---
title: Propriété canonique PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a31b767ef02e12dced9e2a43f9cdba7f2a4e220
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574944"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Propriété canonique PidTagOriginatorDeliveryReportRequested

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un expéditeur de message demande une note de remise pour un destinataire particulier au système de messagerie avant que le message ne soit placé dans la boutique de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0023  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages remis. Dans ce cas, le message doit également fournir la **propriété PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) définie sur FALSE.
  
Définir la **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** d’un message est un moyen de demander des rapports d’état de remise pour tous les destinataires. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
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

