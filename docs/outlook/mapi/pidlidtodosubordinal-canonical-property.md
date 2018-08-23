---
title: Propriété canonique PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 98dfdab24d2c4170609d9db1c3104a3f17436736
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578065"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>Propriété canonique PidLidToDoSubOrdinal

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Agit comme un séparateur de jonction lorsque la propriété **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) trie les objets et le résultat dans un lien.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToDoSubOrdinal  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x000085A1  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

En cas d’utilisation, cette propriété doit être triée lexicographiquement. Les caractères d’un composant de la chaîne doivent contenir uniquement les chiffres zéro à neuf. Cette propriété doit être définie à l’origine pour « 5555555 ». La longueur de cette propriété ne doit pas dépasser 254 caractères (à l’exception du caractère de fin NULL).
  
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



[Propriété canonique PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

