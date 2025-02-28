---
title: Exemple de flux PropertyDefinition
description: Cette rubrique décrit un exemple de flux PropertyDefinition, qui contient une définition d’un champ défini par l’utilisateur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
ms.openlocfilehash: 514bbf8fef7f63d351928c5490d1cd8bfd075f0c
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752364"
---
# <a name="propertydefinition-stream-sample"></a>Exemple de flux PropertyDefinition

**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette rubrique décrit un exemple de flux PropertyDefinition. Le flux contient une définition d’un champ défini par l’utilisateur. `TextField1` Le type est **Text** et la définition est au format PropDefV2.
  
## <a name="data-dump"></a>Vidage des données

Voici un vidage de données du flux tel qu’il serait affiché dans un éditeur binaire.
  
|Décalage de flux|Octets de données|Données ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |

Voici une analyse des exemples de données pour le flux PropertyDefinition :
  
- Version : Offset 0x0, 2 octets : 0x0103 (PropDefV2).

- FieldDefinitionCount : Offset 0x2, 4 octets : 0x1 (1).

- FieldDefinitions : Offset 0x6, tableau de 1 flux FieldDefinition.

  - Indicateurs : 0x6 de décalage, 4 octets : 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).

  - VT : Décalage 0xA, 2 octets : 0x8 (**VT_BSTR**).

  - DispId : Décalage 0xC, 4 octets : 0x0 (0).

  - NmidNameLength : Offset 0x10, 2 octets : 0xA (10).

  - NmidName : Offset 0x12, tableau de 10 WCHAR. Valeur de chaîne Unicode : « TextField1 ».

  - NameANSI : Offset 0x26, PackedAnsiString stream.

    - Longueur : offset 0x26, 1 octet : 0xA (10).

    - Caractères : Décalage 0x27, tableau de 10 RCHA. Valeur de chaîne ANSI : « TextField1 ».

  - FormulaANSI : Offset 0x31, PackedAnsiString stream.

    - Longueur : offset 0x31, 1 octet : 0x0 (0).

    - Caractères : décalage 0x32, tableau de 0 RCHA. Chaîne ANSI vide.

  - ValidationRuleANSI : Offset 0x32, PackedAnsiString stream.

    - Longueur : 0x32 de décalage, 1 octet : 0x0 (0).

    - Caractères : Décalage 0x33, tableau de 0 RCHA. Chaîne ANSI vide.

  - ValidationTextANSI : Offset 0x33, packedAnsiString stream.

    - Longueur : offset 0x33, 1 octet : 0x0 (0).

    - Caractères : Décalage 0x34, tableau de 0 RCHA. Chaîne ANSI vide.

  - ErrorANSI : Offset 0x34, PackedAnsiString stream.

    - Longueur : offset 0x34, 1 octet : 0x0 (0).

    - Caractères : Décalage 0x35, tableau de 0 RCHA. Chaîne ANSI vide.

  - InternalType : Offset 0x35, 4 octets : 0x0 (iTypeString).

  - SkipBlocks : Offset 0x39, série de flux SkipBlock.

  - First SkipBlock

    - Taille : décalage 0x39, 4 octets : 0x15 (21).

    - Contenu : Offset 0x3D, tableau de 21 octets. Comme il s’agit du premier flux SkipBlock, ce tableau contient un flux FirstSkipBlockContent.

      - FieldName : Offset 0x3D, PackedUnicodeString stream.

        - Longueur : offset 0x3D, 1 octet : 0xA (10).

        - Caractères : Décalage 0x3E, tableau de 10 WCHAR. Valeur de chaîne Unicode : « TextField1 ».

  - Second SkipBlock

    - Taille : Décalage 0x52, 4 octets : 0x0 (0). Il s’agit du flux SkipBlock qui se termine.

## <a name="see-also"></a>Voir aussi

- [Outlook éléments et champs](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [SkipBlock Stream, structure](skipblock-stream-structure.md)
- [FirstSkipBlockContent Stream, structure](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString Stream, structure](packedansistring-stream-structure.md)
- [PackedUnicodeString Stream Structure](packedunicodestring-stream-structure.md)
