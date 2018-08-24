---
title: Exemple de flux de la définition PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fc216302cb68be4b0e9d57f60f491adebcba1975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573928"
---
# <a name="propertydefinition-stream-sample"></a>Exemple de flux de la définition PropertyDefinition

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit un exemple d’un flux de la définition PropertyDefinition. Le flux contient une définition d’un champ défini par l’utilisateur, `TextField1`. Le type est **texte**, et la définition est au format PropDefV2.
  
## <a name="data-dump"></a>Vidage des données

Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.
  
|Décalage de flux|Octets de données|Données ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Vous trouverez ci-dessous une analyse des données pour le flux de la définition PropertyDefinition :
  
- Version : Décalage de 0 x 0, 2 octets : 0x0103 (PropDefV2).
    
- FieldDefinitionCount : Décalage 0 x 2, 4 octets : 0 x 1 (1).
    
- FieldDefinitions : Décalage 0 x 6, tableau des flux de FieldDefinition 1.
    
  - Indicateurs : Décalage 0 x 6, 4 octets : 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT : Décalage 0xA, 2 octets : 0 x 8 (**VT_BSTR**).
    
  - DispId : Décalage 0xC, 4 octets : 0 x 0 (0).
    
  - NmidNameLength : Décalage de 0 x 10, 2 octets : 0xA (10).
    
  - NmidName : Décalage 0 x 12, tableau de 10 WCHAR. Valeur de chaîne Unicode : « TextField1 ».
    
  - NameANSI : Décalage 0 x 26, PackedAnsiString flux.
    
    - Longueur : Décalage de la 0 x 26, 1 octet : 0xA (10).
      
    - De caractères : Décalage 0 x 27, tableau de 10 caractères. Valeur de chaîne ANSI : « TextField1 ».
    
  - FormulaANSI : Décalage 0 x 31, PackedAnsiString flux.
    
    - Longueur : Décalage de la 0 x 31, 1 octet : 0 x 0 (0).
      
    - De caractères : Décalage 0 x 32, tableau de caractères de 0. Chaîne ANSI vide.
    
  - ValidationRuleANSI : Décalage 0 x 32, PackedAnsiString flux.
    
    - Longueur : Décalage de la 0 x 32, 1 octet : 0 x 0 (0).
      
    - De caractères : Décalage 0 x 33, tableau de caractères de 0. Chaîne ANSI vide.
    
  - ValidationTextANSI : Décalage 0 x 33, PackedAnsiString flux.
    
    - Longueur : Décalage de la 0 x 33, 1 octet : 0 x 0 (0).
      
    - De caractères : Décalage 0 x 34, tableau de caractères de 0. Chaîne ANSI vide.
    
  - ErrorANSI : Décalage 0 x 34, PackedAnsiString flux.
    
    - Longueur : Décalage de la 0 x 34, 1 octet : 0 x 0 (0).
      
    - Caractères : Décalage 0x35, du tableau de caractères de 0. Chaîne ANSI vide.
    
  - InternalType : Décalage 0x35, 4 octets : 0 x 0 (iTypeString).
    
  - SkipBlocks : Décalage 0 x 39, série de flux de données SkipBlock.
    
  - Première SkipBlock
    
    - Taille : Décalage 0 x 39, 4 octets : 0x15 (21).
      
    - Contenu : Décalage 0x3D, tableau d’octets 21. Il s’agit du premier flux SkipBlock, afin que ce tableau contient un flux FirstSkipBlockContent.
      
      - FieldName : Décalage 0x3D, PackedUnicodeString flux.
        
        - Durée : Décalage 0x3D, 1 octet : 0xA (10).
          
        - De caractères : Décalage 0x3E, tableau de 10 WCHAR. Valeur de chaîne Unicode : « TextField1 ».
    
  - Deuxième SkipBlock
    
    - Taille : Décalage 0 x 52, 4 octets : 0 x 0 (0). Il s’agit du flux SkipBlock rencontrée.
    
## <a name="see-also"></a>Voir aussi

- [Champs et éléments Outlook](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

