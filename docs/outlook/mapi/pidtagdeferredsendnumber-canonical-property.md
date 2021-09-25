---
title: Propriété canonique PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3e03f3762f913beb290147b9395fd3c5367d4a55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613540"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Propriété canonique PidTagDeferredSendNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre qui peut être utilisé pour calculer le report de l’envoi d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Identificateur :  <br/> |0x3FEB  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour calculer la propriété **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) lorsqu’elle n’est pas présente. Lorsque l’envoi d’un message est différé, la propriété **PR_DEFERRED_SEND_NUMBER** doit être définie avec la propriété **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), si la propriété **PR_DEFERRED_SEND_TIME** est absente. 
  
La **PR_DEFERRED_SEND_NUMBER** doit être définie entre 0 et 999. 
  
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

