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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786674"
---
# <a name="pidtagrulestate-canonical-property"></a>Propriété canonique PidTagRuleState

  
  
**S’applique à**: Outlook 
  
Une valeur est interprétée comme une combinaison de masque de bits d’indicateurs qui spécifient l’état de la règle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_STATE  <br/> |
|Identificateur :  <br/> |0x6677  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant définit les valeurs possibles de cette propriété.
  
Fr-fr (ST_ENABLED, masque de bits 0 x 00000001)
  
> La règle est activée pour l’exécution. Si cet indicateur n’est pas défini, le serveur doit ignorer cette règle lors de l’évaluation des règles.
    
Restauration d’urgence (ST_ERROR, masque de bits 0 x 00000002)
  
> Le serveur a rencontré une erreur de traitement de la règle.
    
DE (ST_ONLY_WHEN_OOF, masque de bits 0 x 00000004)
  
> La règle est exécutée uniquement lorsque l’utilisateur définit l’état d’absence du bureau (OOF) dans la boîte aux lettres. Cet indicateur ne doit pas être défini dans une règle de dossier public.
    
HI (ST_KEEP_OOF_HIST, masque de bits 0 x 00000008)
  
> Cet indicateur ne doit pas être défini dans une règle de dossier public.
    
EL (ST_EXIT_LEVEL, masque de bits 0 x 00000010)
  
> Évaluation de la règle se termine après l’exécution de cette règle, à l’exception d’évaluation des règles d’absence du bureau.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, masque de bits 0 x 00000020)
  
> Évaluation de cette règle peut être ignorée.
    
PE (ST_RULE_PARSE_ERROR, masque de bits 0 x 00000040)
  
> Le serveur a rencontré une erreur de l’analyse des données règle fournies par le client.
    
X 
  
> N’est pas utilisé par ce protocole. Ce bit ne doit pas être modifié par le client.
    
Indicateurs de note sur l’interaction entre ST_ONLY_WHEN_OOF et ST_EXIT_LEVEL : 
  
Lorsque l’état « d’absence du bureau » est définie sur la boîte aux lettres, et une condition a la valeur TRUE, 
  
ET :
  
- La règle a l’indicateur ST_EXIT_LEVEL défini et l’indicateur ST_ONLY_WHEN_OOF n’est pas définie. Puis, le serveur ne doit pas évaluer les règles suivantes qui n’ont pas ST_ONLY_WHEN_OOF l’indicateur est défini et doit prendre les règles suivantes qui indicateur ST_ONLY_WHEN_OOF ont été défini.
    
OR :
  
- La règle possède à la fois les ST_EXIT_LEVEL ST_ONLY_WHEN_OOF indicateurs et définir. Puis, le serveur ne doit pas évaluer toutes les règles suivantes.
    
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

