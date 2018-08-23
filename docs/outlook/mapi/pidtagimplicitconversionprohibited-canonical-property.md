---
title: Propriété canonique PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571842"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propriété canonique PidTagImplicitConversionProhibited

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si un message transfert agent d’est interdite d’effectuer des conversions de texte message implicite.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x0016  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété a la valeur TRUE, le système de messagerie doit effectuent pas de conversion de contenu dans le message, sauf si elle est demandée explicitement sur une base par destinataire avec la propriété **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

