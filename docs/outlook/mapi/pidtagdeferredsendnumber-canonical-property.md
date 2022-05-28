---
title: Propriété canonique PidTagDeferredSendNumber
description: Décrit la propriété canonique PidTagDeferredSendNumber, qui contient un nombre qui peut être utilisé pour calculer le report de l’envoi d’un message.
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
ms.openlocfilehash: e440ee0ac0c6c3850583db722eda3d3d2e379153
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769276"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Propriété canonique PidTagDeferredSendNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre qui peut être utilisé pour calculer le report de l’envoi d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Identificateur :  <br/> |0x3FEB  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour calculer la propriété **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) lorsqu’elle n’est pas présente. Lorsque l’envoi d’un message est différé, la propriété **PR_DEFERRED_SEND_NUMBER** doit être définie avec la propriété **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) si la propriété **PR_DEFERRED_SEND_TIME** est absente. 
  
La valeur **PR_DEFERRED_SEND_NUMBER** doit être définie entre 0 et 999. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

