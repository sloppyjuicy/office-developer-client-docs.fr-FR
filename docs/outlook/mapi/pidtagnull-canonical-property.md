---
title: Propriété canonique PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: Représente une valeur null ou un paramètre d’une propriété ou réserve de l’espace de tableau. Cela permet de remplir les propriétés calculées de manière peu coûteuse.
ms.openlocfilehash: b2c7a0ae5228016e24c9396e48c09372feb18b86
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523505"
---
# <a name="pidtagnull-canonical-property"></a>Propriété canonique PidTagNull

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente une valeur null ou un paramètre d’une propriété ou réserve de l’espace de tableau.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NULL  <br/> |
|Identificateur :  <br/> |0x0000  <br/> |
|Type de données :  <br/> |PT_NULL  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet de réserver de l’espace dans des tableaux de structures [SPropValue](spropvalue.md) . Il est utilisé dans un tableau de structures [SPropTagArray](sproptagarray.md) pour indiquer à la méthode de réserver de l’espace dans le tableau renvoyé de structures **SPropValue** . Cela permet de remplir les propriétés calculées de manière peu coûteuse. 
  
Pour plus d’informations, voir [Vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md).
  
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

