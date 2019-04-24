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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331443"
---
# <a name="pidnamecrossreference-canonical-property"></a>Propriété canonique PidNameCrossReference

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de champ d'en-tête RFC3282] XREF.
  
|||
|:-----|:-----|
|Noms conviviaux:  <br/> |Aucun  <br/> |
|Jeu de propriétés:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété:  <br/> |Crois  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message extensions) doivent écrire la valeur souhaitée dans un champ d'en-tête XRef. Les lecteurs MIME doivent copier la valeur d'un champ d'en-tête XRef à la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

