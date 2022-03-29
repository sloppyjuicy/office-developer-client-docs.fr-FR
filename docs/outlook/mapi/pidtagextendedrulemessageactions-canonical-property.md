---
title: Propriété canonique PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6845172ac0c17c9ed707ba4886474ed78712bb3e
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454844"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>Propriété canonique PidTagExtendedRuleMessageActions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations supplémentaires sur les propriétés nommées utilisées dans un message FAI (Folder Associated Information).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Identificateur :  <br/> |0x0E99  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur un message FAI. Cette propriété a le même objectif que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mais contient des informations supplémentaires sur la version de la règle et les propriétés nommées stockées dans l’action de règle, ainsi que des informations sur les actions à effectuer par cette règle. Toutes les valeurs de chaîne contenues dans n’importe quelle partie de la mémoire tampon d’action utilisée pour contenir des actions doivent être au format Unicode.
  
Pour plus d’informations sur le format de cette propriété binaire, voir [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
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

