---
title: PidTagExpiryNumber, propriété canonique
description: Décrit la propriété canonique PidTagExpiryNumber, qui définit l’heure d’envoi d’expiration conjointement avec la propriété PR_EXPIRY_UNITS.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
ms.openlocfilehash: 7035af38b36972ebab353d0b43d0219bf0f023d2
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769416"
---
# <a name="pidtagexpirynumber-canonical-property"></a>PidTagExpiryNumber, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l’heure d’envoi d’expiration conjointement avec la propriété **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_NUMBER  <br/> |
|Identificateur :  <br/> |0x3FED  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être comprise entre 0 et 999 inclus, si elle est présente.
  
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

