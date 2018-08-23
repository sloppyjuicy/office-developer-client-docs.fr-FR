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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b19f36337459753e153a96021b1d70308b374bed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577757"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propriété canonique PidLidToDoOrdinalDate

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détermine l’ordre de tri des objets dans une liste de tâches consolidée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoOrdinalDate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x000085A0  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un objet est marqué, cette propriété doit être définie à l’heure actuelle en temps universel coordonné (UTC). 
  
Si le client permet à un utilisateur réorganiser les tâches dans la liste des tâches consolidée par le biais de déplacement ou d’autres mécanismes, ils peuvent utiliser n’importe quel algorithme approprié pour déterminer la nouvelle valeur de cette propriété afin que la tâche s’affiche dans l’emplacement correct lorsque cette propriété est utilisée comme un trier champ Ting.
  
Lorsque cette propriété est utilisée pour trier les objets et les tri des résultats d’égalité, la propriété **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) est utilisée comme un séparateur de jonction.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

