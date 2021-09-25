---
title: Exemple de flux FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eed1ad0e1f64af5bf07cc0ca3c842eed10c43c47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561788"
---
# <a name="folderuserfields-stream-sample"></a>Exemple de flux FolderUserFields

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit un exemple de flux FolderUserFields. Le flux contient une définition d’un champ défini par l’utilisateur,  `TextField1` . Le type est **Texte** et le flux FolderUserFields contient les parties FolderUserFieldsAnsi et FolderUserFieldsUnicode. Pour plus d’informations, [voir Structures de flux de champs de dossier.](folder-fields-stream-structures.md)
  
## <a name="data-dump"></a>Vidage de données

Voici un vidage de données du flux tel qu’il serait affiché dans un éditeur binaire.
  
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
   

Voici une analyse des exemples de données pour le flux **FolderUserFields** :
  
- FolderUserFieldsAnsi : décalage 0x0.
    
  - FieldDefinitionCount : Décalage 0x0, 4 octets : 0x00000002 (2).
    
  - FieldDefinitions : Offset 0x4, tableau de 2 flux FolderFieldDefinitionA.
    
    **Premier élément de tableau**:
    
    - Type de champ : décalage 0x4, 4 octets : 0x00000001 (ftString).
      
    - FieldNameLength : décalage 0x8, 2 octets : 0x000A (10)
      
    - FieldName : décalage 0xA, tableau de 10 chars. Valeur de chaîne ANSI : « TextField1 ».
      
    - Courant : décalage 0x14.
    
      - PropSetGuid : Décalage 0x14, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm : décalage 0x24, 4 octets : 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString : décalage 0x28, 4 octets : 0x00000000.
        
      - dwBitmap : décalage 0x2C, 4 octets : 0x00000000.
        
      - dwDisplay : décalage 0x30, 4 octets : 0x00000000.
        
      - iFmt : Décalage 0x34, 4 octets : 0x00000000.
        
      - wszFormulaLength : Décalage 0x38, 2 octets : 0x0000 (0).
        
      - wszFormula : Offset 0x3A, tableau de 0 WCHARs. Valeur de chaîne vide.
    
    **Deuxième élément de tableau**:
    
    - FieldType : décalage 0x3A, 4 octets : 0x00000000 (ftNone).
      
    - FieldNameLength : Décalage 0x3E, 2 octets : 0x0000 (0).
      
    - FieldName : Décalage 0x40, tableau de 0 CHAR. Valeur de chaîne vide.
      
    - Courant : décalage 0x40.
    
      - PropSetGuid : Décalage 0x40, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm : Décalage 0x50, 4 octets : 0x00000000 (0).
        
      - dwString : décalage 0x54, 4 octets : 0x00000000.
        
      - dwBitmap : décalage 0x58, 4 octets : 0x00000000.
        
      - dwDisplay : décalage 0x5C, 4 octets : 0x00000000.
        
      - iFmt : Décalage 0x60, 4 octets : 0x00000000.
        
      - wszFormulaLength : Décalage 0x64, 2 octets : 0x0000 (0).
        
      - wszFormula : Offset 0x66, tableau de 0 WCHARs. Valeur de chaîne vide.
    
- FolderUserFieldsUnicode : Offset 0x66.
    
  - FieldDefinitionCount : Décalage 0x66, 4 octets : 0x00000002 (2).
    
  - FieldDefinitions : Offset 0x6A, tableau de 2 flux FolderFieldDefinitionW.
    
    **Premier élément de tableau**:
    
    - Type de champ : décalage 0x6A, 4 octets : 0x00000001 (ftString).
      
    - FieldNameLength : Décalage 0x6E, 2 octets : 0x000A (10).
      
    - FieldName : Offset 0x70, tableau de 10 WCHARs. Valeur de chaîne Unicode : « TextField1 ».
      
    - Courant : décalage 0x84.
    
      - PropSetGuid : Décalage 0x84, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm : décalage 0x94, 4 octets : 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString : décalage 0x98, 4 octets : 0x00000000.
        
      - dwBitmap : décalage 0x9C, 4 octets : 0x00000000.
        
      - dwDisplay : décalage 0xA0, 4 octets : 0x00000000.
        
      - iFmt : décalage 0xA4, 4 octets : 0x00000000.
        
      - wszFormulaLength : Décalage 0xA8, 2 octets : 0x0000 (0).
        
      - wszFormula : Offset 0xAA, tableau de 0 WCHARs. Valeur de chaîne vide.
    
    **Deuxième élément de tableau**:
    
    - FieldType : décalage 0xAA, 4 octets : 0x00000000 (ftNone).
      
    - FieldNameLength : Décalage 0xAE, 2 octets : 0x0000 (0).
      
    - FieldName : Offset 0xB0, tableau de 0 WCHARs. Valeur de chaîne vide.
      
    - Courant : décalage 0xB0.
    
      - PropSetGuid : décalage 0xB0, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm : décalage 0xC0, 4 octets : 0x00000000 (0).
        
      - dwString : décalage 0xC4, 4 octets : 0x00000000.
        
      - dwBitmap : décalage 0xC8, 4 octets : 0x00000000.
        
      - dwDisplay : décalage 0xCC, 4 octets : 0x00000000.
        
      - iFmt : Décalage 0xD0, 4 octets : 0x00000000.
        
      - wszFormulaLength : Décalage 0xD4, 2 octets : 0x0000 (0).
        
      - wszFormula : Offset 0xD6, tableau de 0 WCHARs. Valeur de chaîne vide.
    
## <a name="see-also"></a>Voir aussi

- [Outlook Éléments et champs](outlook-items-and-fields.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString Stream Structure](packedansistring-stream-structure.md)
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

