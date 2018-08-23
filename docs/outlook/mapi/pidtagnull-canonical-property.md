---
title: Propriété canonique PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: efb0812a88ad435c2456a729a6e950b371cc0250
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595348"
---
# <a name="pidtagnull-canonical-property"></a>Propriété canonique PidTagNull

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Représente un paramètre d’une propriété ou une valeur null ou réserve de l’espace de tableau.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NULL  <br/> |
|Identificateur :  <br/> |0x0000  <br/> |
|Type de données :  <br/> |PT_NULL  <br/> |
|Domaine :  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour réserver un espace dans les tableaux de structures [SPropValue](spropvalue.md) . Il est utilisé dans un tableau de structures [SPropTagArray](sproptagarray.md) pour indiquer la méthode à réserver un espace dans le tableau retourné des structures **SPropValue** . Ainsi, pour les propriétés calculées à remplir de manière économique. 
  
Pour plus d’informations, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelle.
    
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

