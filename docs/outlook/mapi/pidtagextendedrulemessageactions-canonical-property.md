---
title: Propriété canonique PidTagExtendedRuleMessageActions
description: Décrit la propriété canonique PidTagExtendedRuleMessageActions, qui contient des informations supplémentaires sur les propriétés nommées utilisées dans un message FAI.
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
ms.openlocfilehash: 2839ecb2d455d23b8d336d7639fc68e5be5e01b4
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771131"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>Propriété canonique PidTagExtendedRuleMessageActions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations supplémentaires sur les propriétés nommées utilisées dans un message d’informations associées au dossier (FAI).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Identificateur :  <br/> |0x0E99  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur un message FAI. Cette propriété sert le même objectif que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mais contient des informations supplémentaires sur la version de la règle et les propriétés nommées stockées dans l’action de règle, ainsi que des informations sur les actions à effectuer par cette règle. Toutes les valeurs de chaîne contenues dans n’importe quelle partie de la mémoire tampon d’action utilisée pour contenir des actions doivent être au format Unicode.
  
Pour plus d’informations sur le format de cette propriété binaire, consultez [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

