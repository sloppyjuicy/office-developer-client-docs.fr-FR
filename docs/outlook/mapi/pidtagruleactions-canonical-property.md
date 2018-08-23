---
title: Propriété canonique PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ede62c792b1241a150c9d0a05adbe47fe0b6c0e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567460"
---
# <a name="pidtagruleactions-canonical-property"></a>Propriété canonique PidTagRuleActions

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’ensemble des actions associées à la règle. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_ACTIONS  <br/> |
|Identificateur :  <br/> |0x6680  <br/> |
|Type de données :  <br/> |PT_ACTIONS  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Les actions sont exprimées en tant qu’une action de la règle et le tampon de valeur de propriété contient la structure de mémoire tampon règle action données empaquetée tel que spécifié dans [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ImportProcs.cpp  <br/> |PropCopyMore, HrCopyActions  <br/> |Ces fonctions vous montrer comment analyser une propriété PT_ACTIONS à des fins de copie vers une autre propriété.  <br/> |
   
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

