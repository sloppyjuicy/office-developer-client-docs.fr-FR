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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329266"
---
# <a name="pidtagnull-canonical-property"></a>Propriété canonique PidTagNull

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente une valeur null ou un paramètre d’une propriété ou réserve de l’espace de tableau.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NULL  <br/> |
|Identificateur :  <br/> |0x0000  <br/> |
|Type de données :  <br/> |PT_NULL  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet de réserver de l’espace dans des tableaux de structures [SPropValue.](spropvalue.md) Il est utilisé dans un tableau de structures [SPropTagArray](sproptagarray.md) pour indiquer à la méthode de réserver de l’espace dans le tableau renvoyé de structures **SPropValue.** Cela permet de remplir les propriétés calculées de manière peu coûteuse. 
  
Pour plus d’informations, voir [Vue d’ensemble du type de propriété MAPI.](mapi-property-type-overview.md)
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

