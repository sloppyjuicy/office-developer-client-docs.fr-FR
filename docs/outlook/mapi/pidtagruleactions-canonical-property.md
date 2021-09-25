---
title: Propriété canonique PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c9b750a1cf6a1e393ecff05d1acaf5b2819c24f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563342"
---
# <a name="pidtagruleactions-canonical-property"></a>Propriété canonique PidTagRuleActions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ensemble des actions associées à la règle. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_ACTIONS  <br/> |
|Identificateur :  <br/> |0x6680  <br/> |
|Type de données :  <br/> |PT_ACTIONS  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Les actions sont exprimées sous la forme d’une action de règle et la mémoire tampon de valeur de propriété contient la structure de tampon de données d’action de règle empaqueté comme spécifié dans [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ImportProcs.cpp  <br/> |PropCopyMore, HrCopyActions  <br/> |Ces fonctions montrent comment PT_ACTIONS une propriété à des fins de copie dans une autre propriété.  <br/> |
   
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

