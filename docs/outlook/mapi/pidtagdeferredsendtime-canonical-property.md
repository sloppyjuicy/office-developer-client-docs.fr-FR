---
title: Propriété canonique PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397204"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>Propriété canonique PidTagDeferredSendTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique une heure lorsqu’un client souhaite différer l’envoi d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|Identificateur :  <br/> |0x3FEF  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si les **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) et les propriétés de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) sont présentes, la valeur de cette propriété est recalculée à l’aide de la formule suivante et l’ancienne valeur est ignorée.
  
 **PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * heure (**PR_DEFERRED_SEND_UNITS**)
  
Si la valeur **PR_DEFERRED_SEND_TIME** est antérieure à l’heure actuelle (en UTC), le message est envoyé immédiatement. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

