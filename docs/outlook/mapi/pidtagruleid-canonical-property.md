---
title: Propriété canonique PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9b8cca70214543658f708beb81785617d79406c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624558"
---
# <a name="pidtagruleid-canonical-property"></a>Propriété canonique PidTagRuleId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un identificateur unique que le serveur de messagerie génère pour chaque règle lors de la création de la règle. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_ID  <br/> |
|Identificateur :  <br/> |0x6674  <br/> |
|Type de données :  <br/> |PT_I8  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le client ne doit pas spécifier cette propriété lors de la création d’une règle, mais doit la spécifier lors de la modification ou de la suppression d’une règle.
  
Lors de la suppression d’une règle, la seule propriété que le client doit transmettre **est PR_RULE_ID** et ne doit pas transmettre d’autre propriété. Le serveur doit ignorer les propriétés autres que cette propriété. Lors de l’ajout d’une règle, le client ne doit pas transmettre **PR_RULE_ID**, il doit passer les propriétés **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) et **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)). Lors de la modification d’une règle, le client doit transmettre **PR_RULE_ID** et transmettre le reste des propriétés qui doivent être modifiées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propriété canonique PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propriété canonique PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

