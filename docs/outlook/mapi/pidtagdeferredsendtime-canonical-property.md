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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359877"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>Propriété canonique PidTagDeferredSendTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le moment où un client souhaite différer l'envoi d'un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|Identificateur :  <br/> |0x3FEF  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si les propriétés **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) et **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) sont présentes, la valeur de cette propriété est recalculée à l'aide de la formule suivante et l'ancienne valeur est ignorée.
  
 **PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * TimeOf (**PR_DEFERRED_SEND_UNITS**)
  
Si la valeur de **PR_DEFERRED_SEND_TIME** est antérieure à l'heure actuelle (UTC), le message est envoyé immédiatement. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

