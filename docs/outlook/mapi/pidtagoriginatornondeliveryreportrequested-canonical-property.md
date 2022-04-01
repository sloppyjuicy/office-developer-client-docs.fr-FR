---
title: Propriété canonique PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: Contient TRUE si un expéditeur de message demande un rapport de non-destinataire pour un destinataire particulier pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 4122b359a03b929ad11a062e611755c89c201527
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523841"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a>Propriété canonique PidTagOriginatorNonDeliveryReportRequested

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un expéditeur de message demande un rapport de non-delivery pour un destinataire particulier.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0C08  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages non envoyés. Dans ce cas, le message doit également fournir la **propriété PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) définie sur FALSE.
  
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

