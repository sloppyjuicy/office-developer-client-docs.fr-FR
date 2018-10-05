---
title: Propriété canonique PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401656"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>Propriété canonique PidTagExtendedRuleMessageCondition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur les propriétés nommées qui sont contenus dans des conditions de règle d’étendue.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|Identificateur :  <br/> |0x0E9A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur un message FAI. Il remplit la même fonction que **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), mais il contient des informations supplémentaires sur les propriétés nommées utilisé. Toutes les valeurs de chaîne contenues dans n’importe quelle partie de cette valeur de la propriété condition doivent être au format Unicode.
  
Pour plus d’informations sur le format de cette propriété binaire, voir [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

