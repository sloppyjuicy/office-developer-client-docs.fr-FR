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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345275"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propriété canonique PidLidToDoOrdinalDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine l'ordre de tri des objets dans une liste de tâches consolidée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoOrdinalDate  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Common  <br/> |
|ID long (couvercle):  <br/> |0x000085A0  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu'un objet est marqué, cette propriété doit être définie sur l'heure actuelle au format UTC (Coordinated Universal Time, temps universel coordonné). 
  
Si le client permet à un utilisateur de réorganiser les tâches au sein de la liste de tâches consolidée via le glisser-déplacer ou d'autres mécanismes, ils peuvent utiliser n'importe quel algorithme approprié pour déterminer la nouvelle valeur de cette propriété afin que la tâche s'affiche à l'emplacement approprié lorsque cette propriété est utilisée comme SOR champ Ting.
  
Lorsque cette propriété est utilisée pour trier les objets et que le tri a pour résultat une égalité, la propriété **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) est utilisée comme un disjoncteur de liaison.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations relatives au marquage.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

