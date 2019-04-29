---
title: Exemple de flux FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433975"
---
# <a name="folderuserfields-stream-sample"></a>Exemple de flux FolderUserFields

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit un exemple de flux FolderUserFields. Le flux contient une définition d'un champ défini par l'utilisateur `TextField1`,. Le type est **Text**et le flux FolderUserFields contient à la fois des composants FolderUserFieldsAnsi et FolderUserFieldsUnicode. Pour plus d'informations, consultez la rubrique [champs de dossier structures de flux](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Vidage des données

Voici un dump des données du flux tel qu'il s'afficherait dans un éditeur binaire.
  
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
  
- FolderUserFieldsAnsi: offset 0x0.
    
  - FieldDefinitionCount: offset 0x0, 4 octets: 0x00000002 (2).
    
  - FieldDefinitions: offset 0x4, tableau de 2 flux de FolderFieldDefinitionA.
    
    **Premier élément de tableau**:
    
    - FieldType: offset 0x4, 4 octets: 0x00000001 (ftString).
      
    - FieldNameLength: décalage 0x8, 2 octets: 0x000A (10)
      
    - FieldName: offset 0xA, tableau de 10 caractères. Valeur de chaîne ANSI: «TextField1».
      
    - Common: offset 0x14.
    
      - PropSetGuid: offset 0x14, 16 octets: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: offset 0x24, 4 octets: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: décalage 0x28, 4 octets: 0x00000000.
        
      - dwBitmap: décalage 0x2C, 4 octets: 0x00000000.
        
      - dwDisplay: décalage 0x30, 4 octets: 0x00000000.
        
      - iFmt: décalage 0x34, 4 octets: 0x00000000.
        
      - wszFormulaLength: décalage 0x38, 2 octets: 0x0000 (0).
        
      - wszFormula: décalage 0x3A, tableau de 0 WCHARs. Valeur de chaîne vide.
    
    **Deuxième élément de tableau**:
    
    - FieldType: décalage 0x3A, 4 octets: 0x00000000 (ftNone).
      
    - FieldNameLength: décalage 0x3E, 2 octets: 0x0000 (0).
      
    - FieldName: offset 0x40, tableau de 0 CHARs. Valeur de chaîne vide.
      
    - Commun: décalage 0x40.
    
      - PropSetGuid: offset 0x40, 16 octets: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: décalage 0x50, 4 octets: 0x00000000 (0).
        
      - dwString: décalage 0x54, 4 octets: 0x00000000.
        
      - dwBitmap: décalage 0x58, 4 octets: 0x00000000.
        
      - dwDisplay: décalage 0x5C, 4 octets: 0x00000000.
        
      - iFmt: décalage 0x60, 4 octets: 0x00000000.
        
      - wszFormulaLength: décalage 0x64, 2 octets: 0x0000 (0).
        
      - wszFormula: décalage 0x66, tableau de 0 WCHARs. Valeur de chaîne vide.
    
- FolderUserFieldsUnicode: décalage 0x66.
    
  - FieldDefinitionCount: décalage 0x66, 4 octets: 0x00000002 (2).
    
  - FieldDefinitions: décalage 0x6A, tableau de 2 flux de FolderFieldDefinitionW.
    
    **Premier élément de tableau**:
    
    - FieldType: décalage 0x6A, 4 octets: 0x00000001 (ftString).
      
    - FieldNameLength: décalage 0x6E, 2 octets: 0x000A (10).
      
    - Nom_champ: décalage 0x70, tableau de 10 WCHARs. Valeur de chaîne Unicode: «TextField1».
      
    - Common: offset 0x84.
    
      - PropSetGuid: décalage 0x84, 16 octets: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: décalage 0x94, 4 octets: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: décalage 0x98, 4 octets: 0x00000000.
        
      - dwBitmap: décalage 0x9C, 4 octets: 0x00000000.
        
      - dwDisplay: décalage 0xA0, 4 octets: 0x00000000.
        
      - iFmt: décalage 0xA4, 4 octets: 0x00000000.
        
      - wszFormulaLength: décalage 0xA8, 2 octets: 0x0000 (0).
        
      - wszFormula: décalage 0xAA, tableau de 0 WCHARs. Valeur de chaîne vide.
    
    **Deuxième élément de tableau**:
    
    - FieldType: décalage 0xAA, 4 octets: 0x00000000 (ftNone).
      
    - FieldNameLength: décalage 0xAE, 2 octets: 0x0000 (0).
      
    - FieldName: offset 0xB0, tableau de 0 WCHARs. Valeur de chaîne vide.
      
    - Common: offset 0xB0.
    
      - PropSetGuid: décalage 0xB0, 16 octets: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: décalage 0xC0, 4 octets: 0x00000000 (0).
        
      - dwString: décalage 0xC4, 4 octets: 0x00000000.
        
      - dwBitmap: décalage 0xC8, 4 octets: 0x00000000.
        
      - dwDisplay: décalage 0xCC, 4 octets: 0x00000000.
        
      - iFmt: décalage 0xD0, 4 octets: 0x00000000.
        
      - wszFormulaLength: décalage 0xD4, 2 octets: 0x0000 (0).
        
      - wszFormula: décalage 0xD6, tableau de 0 WCHARs. Valeur de chaîne vide.
    
## <a name="see-also"></a>Voir aussi

- [Éléments et champs Outlook](outlook-items-and-fields.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

