---
title: Propriété canonique PidTagRuleCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786651"
---
# <a name="pidtagrulecondition-canonical-property"></a>Propriété canonique PidTagRuleCondition

  
  
**S’applique à**: Outlook 
  
La condition utilisée lors de l’évaluation de la règle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_CONDITION  <br/> |
|Identificateur :  <br/> |0x6679  <br/> |
|Type de données :  <br/> |PT_SRESTRICTION  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

La condition est exprimée sous la forme d’une **Restriction** et la mémoire tampon **PropertyValue** contient la structure de **Restriction** empaquetée tel que spécifié dans [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ImportProcs.cpp  <br/> |PropCopyMore, HrCopyRestriction  <br/> |Ces fonctions vous montrer comment analyser une propriété **PT_SRESTRICTION** à des fins de copie vers une autre propriété.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

