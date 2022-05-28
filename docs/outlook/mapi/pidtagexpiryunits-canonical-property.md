---
title: PidTagExpiryUnits Canonical, propriété
description: Décrit la propriété canonique PidTagExpiryUnits, qui décrit l’unité de temps pendant laquelle la propriété PR_EXPIRY_NUMBER se multiplie.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
ms.openlocfilehash: 57922e87c3ed1882d80b016446aaae6bd3a83700
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769297"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit l’unité de temps pendant laquelle la propriété **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) se multiplie.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificateur :  <br/> |0x3FEE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si elle est définie, doit être l’une des valeurs suivantes :
  
|Propriété |Valeur |
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Description (TimeOf)  <br/> |
|0x00000000  <br/> |Minutes, par exemple 60 secondes  <br/> |
|0x00000001  <br/> |Heures, par exemple 60 x 60 secondes  <br/> |
|0x00000002  <br/> |Jour, par exemple 24 x 60 x 60 secondes  <br/> |
|0x00000003  <br/> |Semaine, par exemple 7 x 24 x 60 x 60 secondes  <br/> |
   
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

