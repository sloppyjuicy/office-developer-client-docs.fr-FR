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
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785971"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propriété canonique PidTagExpiryUnits

  
  
**S’applique à**: Outlook 
  
Décrit l’unité de temps lorsque la propriété **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificateur :  <br/> |0x3FEE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si la valeur, doit être une des valeurs suivantes :
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Description (heure)  <br/> |
|0x00000000  <br/> |Minutes, par exemple 60 secondes.  <br/> |
|0x00000001  <br/> |Heures, par exemple 60 x 60 secondes  <br/> |
|0x00000002  <br/> |Jour, par exemple 24 x 60 x 60 secondes  <br/> |
|0 x 00000003  <br/> |Semaine, par exemple 7x24x60x60 secondes  <br/> |
   
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

