---
title: Propriété canonique PidTagAutoForwarded
description: Décrit la propriété canonique PidTagAutoForwarded, qui contient TRUE si le client demande un champ d’en-tête X-MS-Exchange-Organization-AutoForwarded.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
ms.openlocfilehash: b163a8123574654c6621213d17d5672835a80d20
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818004"
---
# <a name="pidtagautoforwarded-canonical-property"></a>Propriété canonique PidTagAutoForwarded

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si le client demande un champ d’en-tête X-MS-Exchange-Organization-AutoForwarded.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AUTO_FORWARDED  <br/> |
|Identificateur :  <br/> |0x0005  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Rapports généraux  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur FALSE ou n’est pas utilisée, aucun champ d’en-tête X-MS-Exchange-Organization-AutoForwarded n’est créé.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Définit chaque propriété utilisée dans les objets décrits par les documents préfixés MS-OXO.
    
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

