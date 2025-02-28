---
title: Propriété canonique PidTagBodyContentLocation
description: Décrit la propriété canonique PidTagBodyContentLocation, qui contient la valeur d’un champ d’en-tête Content-Location MIME.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
ms.openlocfilehash: 03eba98888f217543a03c0b0c8278a1bb3300a71
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816520"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a>Propriété canonique PidTagBodyContentLocation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur d’un champ d’en-tête Content-Location MIME.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W  <br/> |
|Identificateur :  <br/> |0x1014  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée dans un champ d’en-tête Content-Location sur une entité MIME mappée à un corps de message.
  
Les lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Location sur une telle entité MIME vers la valeur de ces propriétés.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
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

