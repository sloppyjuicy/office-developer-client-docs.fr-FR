---
title: Propriété canonique PidTagExpiryUnits
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: af1c43af154e80205fb2e2335adc27122eb8de86
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63719260"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propriété canonique PidTagExpiryUnits

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit l’unité de temps **pendant PR_EXPIRY_NUMBER de** la propriété ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)).
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificateur :  <br/> |0x3FEE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est définie, cette propriété doit avoir l’une des valeurs suivantes :
  
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

