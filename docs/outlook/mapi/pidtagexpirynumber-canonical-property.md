---
title: Propriété canonique PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385822"
---
# <a name="pidtagexpirynumber-canonical-property"></a>Propriété canonique PidTagExpiryNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le délai d’expiration envoi conjointement avec la propriété **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_NUMBER  <br/> |
|Identificateur :  <br/> |0x3FED  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Valeur de cette propriété doit être définie entre 0 et 999 inclus, s’il est présent.
  
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

