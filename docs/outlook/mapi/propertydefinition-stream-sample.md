---
title: Exemple de flux PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406660"
---
# <a name="propertydefinition-stream-sample"></a>Exemple de flux PropertyDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit un exemple de flux PropertyDefinition. Le flux contient une définition d'un champ défini par l'utilisateur `TextField1`,. Le type est **Text**et la définition est au format PropDefV2.
  
## <a name="data-dump"></a>Vidage des données

Voici un dump des données du flux tel qu'il s'afficherait dans un éditeur binaire.
  
|Décalage de flux|Octets de données|Données ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Voici une analyse des exemples de données pour le flux PropertyDefinition:
  
- Version: offset 0x0, 2 octets: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: offset 0X2, 4 octets: 0x1 (1).
    
- FieldDefinitions: décalage 0x6, tableau de 1 FieldDefinition Stream.
    
  - Flags: décalage 0x6, 4 octets: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: décalage 0xA, 2 octets: 0x8 (**VT_BSTR**).
    
  - DispId: décalage 0xC, 4 octets: 0x0 (0).
    
  - NmidNameLength: offset 0x10, 2 octets: 0xA (10).
    
  - NmidName: offset 0x12, tableau de 10 WCHARs. Valeur de chaîne Unicode: «TextField1».
    
  - NameANSI: décalage 0x26, flux de PackedAnsiString.
    
    - Longueur: décalage 0x26, 1 octet: 0xA (10).
      
    - Caractères: décalage 0x27, tableau de 10 caractères. Valeur de chaîne ANSI: «TextField1».
    
  - FormulaANSI: décalage 0x31, flux de PackedAnsiString.
    
    - Longueur: décalage 0x31, 1 octet: 0x0 (0).
      
    - Caractères: décalage 0x32, tableau de 0 CHARs. Chaîne ANSI vide.
    
  - ValidationRuleANSI: décalage 0x32, PackedAnsiString Stream.
    
    - Longueur: décalage 0x32, 1 octet: 0x0 (0).
      
    - Caractères: décalage 0x33, tableau de 0 CHARs. Chaîne ANSI vide.
    
  - ValidationTextANSI: décalage 0x33, flux de PackedAnsiString.
    
    - Longueur: décalage 0x33, 1 octet: 0x0 (0).
      
    - Caractères: décalage 0x34, tableau de 0 CHARs. Chaîne ANSI vide.
    
  - ErrorANSI: décalage 0x34, flux de PackedAnsiString.
    
    - Longueur: décalage 0x34, 1 octet: 0x0 (0).
      
    - Caractères: décalage 0x35, tableau de 0 CHARs. Chaîne ANSI vide.
    
  - InternalType: décalage 0x35, 4 octets: 0x0 (iTypeString).
    
  - SkipBlocks: décalage 0x39, série de flux de SkipBlock.
    
  - Première SkipBlock
    
    - Taille: décalage 0x39, 4 octets: 0x15 (21).
      
    - Content: offset 0x3D, tableau de 21 octets. Il s'agit du premier flux SkipBlock, de sorte que ce tableau contient un flux de FirstSkipBlockContent.
      
      - FieldName: offset 0x3D, PackedUnicodeString Stream.
        
        - Longueur: décalage 0x3D, 1 octet: 0xA (10).
          
        - Caractères: décalage 0x3E, tableau de 10 WCHARs. Valeur de chaîne Unicode: «TextField1».
    
  - Deuxième SkipBlock
    
    - Taille: décalage 0x52, 4 octets: 0x0 (0). Il s'agit du flux de SkipBlock de terminaison.
    
## <a name="see-also"></a>Voir aussi

- [Éléments et champs Outlook](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

