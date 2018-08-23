---
title: Exemple de flux de données FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 76ad693b05e3989bd64ba66565ae4def22110ad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564898"
---
# <a name="folderuserfields-stream-sample"></a>Exemple de flux de données FolderUserFields

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit un exemple d’un flux FolderUserFields. Le flux contient une définition d’un champ défini par l’utilisateur, `TextField1`. Le type est **texte**, et le flux FolderUserFields contient des composants WebPart à la fois FolderUserFieldsAnsi et FolderUserFieldsUnicode. Pour plus d’informations, voir [Dossier champs Stream Structures](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Vidage des données

Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.
  
|Décalage de flux|Octets de données|Données ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

Vous trouverez ci-dessous une analyse des données pour le flux **FolderUserFields** :
  
- FolderUserFieldsAnsi : Décalage 0 x 0.
    
  - FieldDefinitionCount : Décalage de 0 x 0, 4 octets : 0 x 00000002 (2).
    
  - FieldDefinitions : Décalage 0 x 4, tableau des flux de FolderFieldDefinitionA 2.
    
    **Premier élément du tableau**:
    
    - FieldType : Décalage de 0 x 4, 4 octets : 0 x 00000001 (ftString).
      
    - FieldNameLength : Décalage 0 x 8, 2 octets : 0x000A (10)
      
    - FieldName : Décalage 0xA, tableau de 10 caractères. Valeur de chaîne ANSI : « TextField1 ».
      
    - Courants : Décalage 0 x 14.
    
      - PropSetGuid : Décalage 0 x 14, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm : décalage de 0 x 24, 4 octets : 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString : 0 x 28, 4 octets de décalage : 0 x 00000000.
        
      - dwBitmap : décalage 0x2C, 4 octets : 0 x 00000000.
        
      - dwDisplay : 0 x 30, 4 octets de décalage : 0 x 00000000.
        
      - iFmt : 0 x 34, 4 octets de décalage : 0 x 00000000.
        
      - wszFormulaLength : 0 x 38, 2 octets de décalage : 0 x 0000 (0).
        
      - wszFormula : décalage 0x3A, le tableau de 0 WCHAR. Valeur de chaîne vide.
    
    **Deuxième élément du tableau**:
    
    - FieldType : Décalage 0x3A, 4 octets : 0 x 00000000 (ftNone).
      
    - FieldNameLength : Décalage 0x3E, 2 octets : 0 x 0000 (0).
      
    - FieldName : Décalage 0 x 40, du tableau de caractères de 0. Valeur de chaîne vide.
      
    - Courantes : 0 x 40 décalage.
    
      - PropSetGuid : Décalage 0 x 40, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm : 0 x 50, 4 octets de décalage : 0 x 00000000 (0).
        
      - dwString : 0 x 54, 4 octets de décalage : 0 x 00000000.
        
      - dwBitmap : décalage 0x58, 4 octets : 0 x 00000000.
        
      - dwDisplay : décalage 0x5C, 4 octets : 0 x 00000000.
        
      - iFmt : 0 x 60, 4 octets de décalage : 0 x 00000000.
        
      - wszFormulaLength : 0 x 64, 2 octets de décalage : 0 x 0000 (0).
        
      - wszFormula : décalage 0x66, le tableau de 0 WCHAR. Valeur de chaîne vide.
    
- FolderUserFieldsUnicode : Décalage 0x66.
    
  - FieldDefinitionCount : Décalage 0x66, 4 octets : 0 x 00000002 (2).
    
  - FieldDefinitions : Décalage 0x6A, tableau des flux de FolderFieldDefinitionW 2.
    
    **Premier élément du tableau**:
    
    - FieldType : Décalage 0x6A, 4 octets : 0 x 00000001 (ftString).
      
    - FieldNameLength : Décalage 0x6E, 2 octets : 0x000A (10).
      
    - FieldName : Décalage 0 x 70, tableau de 10 WCHAR. Valeur de chaîne Unicode : « TextField1 ».
      
    - Courantes : 0 x 84 décalage.
    
      - PropSetGuid : Décalage de 0 x 84, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm : décalage 0x94, 4 octets : 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString : décalage 0x98, 4 octets : 0 x 00000000.
        
      - dwBitmap : décalage 0x9C, 4 octets : 0 x 00000000.
        
      - dwDisplay : décalage 0xA0, 4 octets : 0 x 00000000.
        
      - iFmt : décalage 0xA4, 4 octets : 0 x 00000000.
        
      - wszFormulaLength : décalage 0xA8, 2 octets : 0 x 0000 (0).
        
      - wszFormula : décalage 0xAA, le tableau de 0 WCHAR. Valeur de chaîne vide.
    
    **Deuxième élément du tableau**:
    
    - FieldType : Décalage 0xAA, 4 octets : 0 x 00000000 (ftNone).
      
    - FieldNameLength : Décalage 0xAE, 2 octets : 0 x 0000 (0).
      
    - FieldName : Décalage 0xB0, tableau de 0 WCHAR. Valeur de chaîne vide.
      
    - Courantes : Décalage 0xB0.
    
      - PropSetGuid : Décalage 0xB0, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm : décalage 0xC0, 4 octets : 0 x 00000000 (0).
        
      - dwString : décalage 0xC4, 4 octets : 0 x 00000000.
        
      - dwBitmap : décalage 0xC8, 4 octets : 0 x 00000000.
        
      - dwDisplay : décalage 0xCC, 4 octets : 0 x 00000000.
        
      - iFmt : décalage 0xD0, 4 octets : 0 x 00000000.
        
      - wszFormulaLength : décalage 0xD4, 2 octets : 0 x 0000 (0).
        
      - wszFormula : décalage 0xD6, le tableau de 0 WCHAR. Valeur de chaîne vide.
    
## <a name="see-also"></a>Voir aussi

- [Champs et éléments Outlook](outlook-items-and-fields.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

