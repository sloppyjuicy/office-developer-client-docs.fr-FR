---
title: Propriété canonique PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 05fe447b78a0ef4e5e836324a4a8e37124bf5647
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455306"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>Propriété canonique PidTagDeferredSendUnits

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’unité de temps à laquelle la valeur **PR_DEFERRED_SEND_NUMBER propriété (**[PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) doit être multipliée.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Identificateur :  <br/> |0x3FEC  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est définie, cette propriété doit avoir l’une des valeurs suivantes :
  
|**PidTagDeferredSendUnits** <br/> |Description  <br/> |
|:-----|:-----|
|0  <br/> |Minutes, par exemple 60 secondes  <br/> |
|1  <br/> |Heures, par exemple 60 x 60 secondes  <br/> |
|2  <br/> |Jour, par exemple 24 x 60 x 60 secondes  <br/> |
|3  <br/> |Semaine, par exemple 7 x 24 x 60 x 60 secondes  <br/> |
   
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

