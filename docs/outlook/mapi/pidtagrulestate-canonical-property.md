---
title: Propriété canonique PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338611"
---
# <a name="pidtagrulestate-canonical-property"></a>Propriété canonique PidTagRuleState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valeur interprétée comme une combinaison de masques de bits d’indicateurs spécifiant l’état de la règle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_STATE  <br/> |
|Identificateur :  <br/> |0x6677  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant définit les valeurs possibles de cette propriété.
  
EN (ST_ENABLED, masque de bits 0x00000001)
  
> La règle est activée pour l’exécution. Si cet indicateur n’est pas définie, le serveur doit ignorer cette règle lors de l’évaluation des règles.
    
ER (ST_ERROR, masque de bits 0x00000002)
  
> Le serveur a rencontré une erreur lors du traitement de la règle.
    
OF (ST_ONLY_WHEN_OOF, masque de bits 0x00000004)
  
> La règle est exécutée uniquement lorsque l’utilisateur définit l’état Office hors Office la boîte aux lettres. Cet indicateur ne doit pas être définie dans une règle de dossier public.
    
HI (ST_KEEP_OOF_HIST, masque de bits 0x00000008)
  
> Cet indicateur ne doit pas être définie dans une règle de dossier public.
    
EL (ST_EXIT_LEVEL, masque de bits 0x00000010)
  
> L’évaluation de la règle se termine après l’exécution de cette règle, à l’exception de l’évaluation des règles Office hors projet.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, masque de bits 0x00000020)
  
> L’évaluation de cette règle peut être ignorée.
    
PE (ST_RULE_PARSE_ERROR, masque de bits 0x00000040)
  
> Le serveur a rencontré une erreur lors de l’analyse des données de règle fournies par le client.
    
X
  
> Inutilisé par ce protocole. Ce bit ne doit pas être modifié par le client.
    
Notez l’interaction entre ST_ONLY_WHEN_OOF et ST_EXIT_LEVEL indicateurs : 
  
Lorsque l’état « Hors Office » est définie sur la boîte aux lettres et qu’une condition de règle est évaluée à TRUE, 
  
ET :
  
- La règle possède l’indicateur ST_EXIT_LEVEL et n’a pas d’indicateur ST_ONLY_WHEN_OOF définie. Ensuite, le serveur ne doit pas évaluer les règles suivantes qui n’ont pas d’indicateur ST_ONLY_WHEN_OOF, et doit évaluer les règles suivantes qui ont ST_ONLY_WHEN_OOF d’indicateur.
    
OU :
  
- Les indicateurs ST_EXIT_LEVEL et ST_ONLY_WHEN_OOF règle sont tous deux définies. Ensuite, le serveur ne doit pas évaluer les règles suivantes.
    
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

