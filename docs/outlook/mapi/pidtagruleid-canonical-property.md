---
title: Propriété canonique PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786649"
---
# <a name="pidtagruleid-canonical-property"></a>Propriété canonique PidTagRuleId

  
  
**S’applique à**: Outlook 
  
Spécifie un identificateur unique du serveur de messagerie génère pour chaque règle lors de la création de la règle. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_ID  <br/> |
|Identificateur :  <br/> |0x6674  <br/> |
|Type de données :  <br/> |PT_I8  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le client ne doit pas spécifier de cette propriété lorsque vous créez une nouvelle règle mais doit spécifier lors de la modification ou suppression d’une règle.
  
Lorsque vous supprimez une règle, la seule propriété que le client doit transmettre est **PR_RULE_ID** et ne doit pas passer dans n’importe quelle autre propriété. Le serveur doit ignorer les propriétés de cette propriété. Lorsque vous ajoutez une règle, le client ne doit pas passer dans **PR_RULE_ID**, il doit passer **PR_RULE_PROVIDER** ([ , **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) et **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) Propriétés. Lorsque vous modifiez une règle, le client doit passer **PR_RULE_ID** et doit transmettre le reste des propriétés qui doivent être modifiées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propriété canonique PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propriété canonique PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

