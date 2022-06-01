---
title: Propriété canonique PidLidToDoSubOrdinal
description: Décrit la propriété canonique PidLidToDoSubOrdinal, qui joue le rôle de disjoncteur lorsque la propriété dispidToDoOrdinalDate trie les objets et le résultat dans une égalité.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
ms.openlocfilehash: e106d0da5f3c7d415a0ee3964db8dec7a07208c2
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817381"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>Propriété canonique PidLidToDoSubOrdinal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Agit en tant que **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) lorsque la propriété trie les objets et génère un lien.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoSubOrdinal  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085A1  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est utilisée, cette propriété doit être triée lexicographiquement. Les caractères de composant de la chaîne doivent être constitués uniquement des chiffres de zéro à neuf. Cette propriété doit être initialement définie sur « 5555555 ». La longueur de cette propriété ne doit pas dépasser 254 caractères (à l’exception du caractère NULL de fin).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

