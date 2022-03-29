---
title: Propriété canonique PidTagAutoForwarded
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 329be9b73594ff0bc21037802008f6d9501bfa9d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64453990"
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
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
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

