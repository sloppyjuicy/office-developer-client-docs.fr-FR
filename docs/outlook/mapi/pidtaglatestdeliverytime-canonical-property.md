---
title: Propriété canonique PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b248411d52e54c327abb062ede99ee2c4054dd29
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523353"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>Propriété canonique PidTagLatestDeliveryTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure les plus récentes à laquelle un agent de transfert de messages doit remettre un message. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LATEST_DELIVERY_TIME  <br/> |
|Identificateur :  <br/> |0x0019  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Si un MTA ne peut pas remettre un message au moment spécifié par cette propriété, il annule le message sans remise. 
  
## <a name="related-resources"></a>Ressources connexes

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

