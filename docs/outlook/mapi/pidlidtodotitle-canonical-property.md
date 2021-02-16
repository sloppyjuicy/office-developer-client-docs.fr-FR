---
title: Propriété canonique PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339941"
---
# <a name="pidlidtodotitle-canonical-property"></a>Propriété canonique PidLidToDoTitle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le texte spécifié par l’utilisateur pour identifier cet objet de message dans une liste de choses à faire consolidée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoTitle  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085A4  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété ne doit pas être définie sur une tâche. Pour indiquer une propriété vide, ne définissez pas cette propriété sur la chaîne de longueur nulle, mais supprimez-la. 
  
Lorsque vous signalez un objet de message et que la propriété n’existe pas, un client doit écrire la valeur **de PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) dans cette propriété.
  
Dans une liste de choses à faire consolidée, si cette propriété n’existe pas, un client doit remplacer la valeur de la propriété **PR_NORMALIZED_SUBJECT** lors de l’affichage de cette propriété dans la liste des choses à faire. 
  
Sur un objet de brouillon de message, si le client implémente des indicateurs d’expéditeur, cette propriété doit être définie sur la même valeur que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[Propri�t� canonique PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

