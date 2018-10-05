---
title: Propriété canonique PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382497"
---
# <a name="pidnamecrossreference-canonical-property"></a>Propriété canonique PidNameCrossReference

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de champ d’en-tête référence croisée [RFC3282].
  
|||
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucune  <br/> |
|Jeu de propriétés :  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété :  <br/> |Référence croisée  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de cette propriété, clients Message Extensions MIME (Multipurpose Internet) doivent écrire la valeur souhaitée dans un champ d’en-tête référence croisée. Lecteurs MIME doivent copier la valeur d’un champ d’en-tête de référence croisée sur la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

