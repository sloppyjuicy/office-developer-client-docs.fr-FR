---
title: Propriété canonique PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316407"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propriété canonique PidTagExpiryUnits

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit l'unité de temps à laquelle la propriété **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificateur :  <br/> |0x3FEE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si elle est définie, doit avoir l'une des valeurs suivantes:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Description (TimeOf)  <br/> |
|0x00000000  <br/> |Minutes, par exemple 60 secondes  <br/> |
|0x00000001  <br/> |Heures, par exemple 60x60 secondes  <br/> |
|0x00000002  <br/> |Jour, par exemple 24x60x60 secondes  <br/> |
|0x00000003  <br/> |Semaine, par exemple 7x24x60x60 secondes  <br/> |
   
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

