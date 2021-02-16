---
title: Propriété canonique PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345275"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propriété canonique PidLidToDoOrdinalDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine l’ordre de tri des objets dans une liste de choses à faire consolidée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoOrdinalDate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085A0  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un objet est marqué, cette propriété doit être définie sur l’heure actuelle en temps universel coordonné (UTC). 
  
Si le client permet à un utilisateur de réorder les tâches dans la liste des tâches consolidées par glisser-glisser ou d’autres mécanismes, il peut utiliser n’importe quel algorithme approprié pour déterminer la nouvelle valeur de cette propriété afin que la tâche apparaisse à l’endroit approprié lorsque cette propriété est utilisée comme champ de tri.
  
Lorsque cette propriété est utilisée pour trier des objets et que le tri se traduit par une égalité, la propriété **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) est utilisée comme un décomposeur d’égalité.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

