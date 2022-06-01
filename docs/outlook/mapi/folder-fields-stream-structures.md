---
title: Structures de flux de champs de dossier
description: Cet article décrit les structures de flux de champs de dossiers et fournit des éléments de données.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
ms.openlocfilehash: 506643d2f06c4f214b9a0ee8cfbc9fd2ae5ff8b4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817087"
---
# <a name="folder-fields-stream-structures"></a>Structures de flux de champs de dossier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La propriété [PidTagUserFields](pidtaguserfields-canonical-property.md) d’un message contient un flux binaire, FolderUserFields, qui contient les définitions de champ définies par l’utilisateur du dossier. Cette rubrique décrit les structures de flux pour les définitions de champ définies par l’utilisateur du dossier. 

Une structure de flux FolderUserFields se compose d’une structure FolderUserFieldsA ou d’une structure FolderUserFieldsA suivie d’une structure FolderUserFieldsW.
  
Les éléments de données de ce flux sont stockés immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FolderUserFieldsAnsi** : structure de flux FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (facultatif) : structure de flux FolderUserFieldsW.
    
La présence de FolderUserFieldsUnicode est détectée par la longueur totale de FolderUserFields supérieure à la longueur de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi est utilisé pour la compatibilité avec les versions antérieures, non Unicode, des clients MAPI. Par conséquent, si FolderUserFieldsUnicode est présent, le contenu de FolderUserFieldsAnsi est ignoré. Pour éviter toute perte de données dans la conversion ANSI, lors de la création d’un flux FolderUserFields, incluez toujours la partie FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Structure de flux FolderUserFieldsA

Une structure de flux FolderUserFieldsA est un tableau de structures de flux FolderFieldDefinitionA qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook, sauf si elle est remplacée par la partie FolderUserFieldsW de la structure FolderUserFields.
  
Les éléments de données de ce flux sont stockés dans l’ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount** : DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions** : tableau de structures de flux FolderFieldDefinitionA. Le nombre de ce tableau est égal à l’élément de données **FieldDefinitionCount** .
    
À moins que folderUserFieldsA ne soit remplacé par la partie FolderUserFieldsW de la structure FolderUserFields, le tableau **FieldDefinitions** doit être « null-terminateed » en ayant le dernier champ Common.FieldType de son dernier élément FolderFieldDefinitionA égal à ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Structure de flux FolderUserFieldsW

Une structure de flux FolderUserFieldsW est un tableau de structures de flux FolderFieldDefinitionW qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook.
  
Les éléments de données de ce flux sont stockés dans l’ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount** : DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions** : tableau de structures de flux FolderFieldDefinitionW. Le nombre de ce tableau est égal à l’élément de données **FieldDefinitionCount** .
    
Le tableau **FieldDefinitions** doit être « terminé par null » en ayant le champ Common.FieldType de son dernier élément FolderFieldDefinitionW égal à ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Structure de flux FolderFieldDefinitionA

Une structure de flux FolderFieldDefinitionA contient une définition d’un champ défini par l’utilisateur avec le nom de champ stocké dans ANSI.
  
Les éléments de données de ce flux sont stockés dans l’ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié suivant :
  
- **FieldType** : FldType (4 octets), type de ce champ.
    
- **FieldNameLength** : WORD (2 octets), nombre d’éléments dans le tableau **FieldName** .
    
- **FieldName** : tableau de CHAR. Il s’agit de la représentation ansi CP_ACP page de code du nom de champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit respecter les restrictions sur le paramètre Name, comme spécifié dans la méthode [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook pouvez gérer certaines valeurs **FieldName** qui ne satisfaisaient pas à ces restrictions, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **Common** : structure de flux FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Structure de flux FolderFieldDefinitionW

Une structure de flux FolderFieldDefinitionW contient une définition d’un champ défini par l’utilisateur avec le nom de champ stocké dans Unicode.
  
Les éléments de données de ce flux sont stockés dans l’ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié suivant :
  
- **FieldType** : FldType (4 octets), type de ce champ.
    
- **FieldNameLength** : WORD (2 octets), nombre d’éléments dans le tableau **FieldName** .
    
- **FieldName** : tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) du nom du champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit respecter les restrictions sur le paramètre Name, comme spécifié dans la méthode [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook pouvez gérer certaines valeurs **FieldName** qui ne satisfaisaient pas à ces restrictions, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **Common** : structure de flux FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>FldType, énumération

Les valeurs **d’énumération FldType** sont répertoriées dans le tableau suivant. 
  
|Nom|Valeur|Signification|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Ce type de champ est utilisé pour mettre fin à un tableau de définitions de champ. |
|ftString  <br/> |0x1  <br/> |Texte  <br/> |
|ftInteger  <br/> |0x3  <br/> |Entier  <br/> |
|ftTime  <br/> |0x5  <br/> |Date/Heure  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Oui/Non  <br/> |
|ftDuration  <br/> |0x7  <br/> |Durée  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Mots clés  <br/> |
|ftFloat  <br/> |0xC  <br/> |Nombre ou pourcentage  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Devise  <br/> |
|ftCalc  <br/> |0x12  <br/> |Formule  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinaison de type affichant uniquement le premier champ non vide , en ignorant les suivants. |
|ftConcat  <br/> |0x17  <br/> |Combinaison de champs de jointure de type et de fragments de texte les uns aux autres. |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Structure de flux FolderFieldDefinitionCommon

Une structure de flux FolderFieldDefinitionCommon contient les données d’une définition de champ définie par l’utilisateur commune à un FolderFieldDefinitionA et à un FolderFieldDefinitionW.
  
Les éléments de données de ce flux sont stockés dans l’ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié suivant :
  
- **PropSetGuid** : GUID (16 octets), guid du jeu de propriétés du nom de propriété MAPI correspondant du champ de dossier. La valeur de ce champ doit être égale à PS_PUBLIC_STRINGS, sauf si le type de champ est **ftNone** , auquel cas la valeur de ce champ doit être égale à GUID_NULL. 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook pouvez gérer certaines valeurs **PropSetGuid** ne répondant pas à cette restriction, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **fcapm** : DWORD (4 octets), une combinaison de zéro ou plusieurs indicateurs dont les valeurs et les significations sont répertoriées dans le tableau suivant. Les indicateurs avec la même valeur ont des significations dépendantes du type du champ, c’est-à-dire de la valeur FldType.
    
    |Nom de l’indicateur|Valeur|Signification|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Le champ est modifiable. |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Le champ est triable. |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Le champ est groupable. |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Le champ peut contenir plusieurs lignes de texte. |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Ce champ du type ftFloat est un champ de pourcentage. |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Ce champ du type ftTime est un champ d’heure de date uniquement. |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Pour ce champ de type ftInteger, aucune unité n’est autorisée au format d’affichage ; par exemple, des formats tels que « Ordinateur - 640 K... » ne sont pas autorisés. |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Le champ peut être modifié dans l’élément : il s’agit spécifiquement pour les formulaires personnalisés. |
   
- **dwString** : DWORD (4 octets). Consultez la première note suivante.
    
- **dwBitmap** : DWORD (4 octets). Consultez la première note suivante.
    
- **dwDisplay** : DWORD (4 octets). Consultez la première note suivante.
    
- **iFmt** : INT (4 octets). Pour les types de champs qui ont la zone de liste déroulante « Format : » dans les boîtes de dialogue « Nouveau champ », « Modifier le champ » et « Propriétés du champ », index basé sur 0 du format sélectionné dans cette zone de liste déroulante. Pour les types de champs sans cette zone de liste déroulante, il doit s’agir de 0. La valeur du champ ainsi que le type de champ déterminent de façon unique les valeurs des champs **dwString**, **dwBitmap** et **dwDisplay** , consultez la première note suivante.
    
- **wszFormulaLength** : WORD (2 octets), nombre d’éléments dans le tableau **wszFormulaLength** .
    
- **wszFormulaLength** : tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) de la chaîne de formule du champ dans son format standard. Consultez la deuxième note suivante pour obtenir la description des formats standard et d’interface utilisateur de la formule d’un champ. Le nombre de ce tableau est égal à **wszFormulaLength**. La chaîne de formule doit être une chaîne vide, sauf si le type de champ est **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Bien que les valeurs de **dwString**, **dwBitmap** et **dwDisplay** soient déterminées de manière unique en fonction de la valeur **FldType** et de la valeur **iFmt**, qui sont redondantes, leurs valeurs correctes sont toujours nécessaires pour un traitement correct de la définition de champ par Outlook. Il n’existe aucune description simple de l’algorithme qui effectue cette détermination. 
> 
> Par conséquent, pour déterminer quelles valeurs **dwString**, **dwBitmap** et **dwDisplay** correspondent à une valeur **FldType** donnée et à une valeur **iFmt**, effectuez un test en créant un champ défini par l’utilisateur de ce type, et avec ce format sélectionné dans la zone de liste déroulante **Format**, en supposant son applicabilité, examinez le flux **FolderUserFields** résultant que Outlook crée pour ce champ défini par l’utilisateur. 
  
La formule du champ dans son format d’interface utilisateur est modifiée dans la zone de texte **Formule** des dialogues **Nouveau champ**, **Modifier le champ** et **Propriétés** du champ pour le champ défini par l’utilisateur. L’algorithme permettant de convertir une formule du format d’interface utilisateur au format standard dépend du type de champ, comme décrit dans la section suivante : 
- Pour les champs de types **ftCalc** et **ftSwitch**, le format standard pour les champs intégrés, dont les propriétés MAPI correspondantes ne sont pas des propriétés nommées du type MNID\_STRING, est obtenu en remplaçant les fragments de nom de champ, c’est-à-dire `[<field_name>]` par des fragments `[_<field_dispid_decimal>]`. 

  Par exemple, si le format d’interface utilisateur d’une formule pour un champ de type **Formule**, c’est-à-dire **ftCalc**, avec la langue de l’interface utilisateur Office étant l’anglais des États-Unis, est `[Business Phone] & [My custom field]`, où `My custom field` est le nom d’un champ défini par l’utilisateur, le format standard d’une telle formule serait `[_14856] & [My custom field]`.

- Pour les champs de type **ftConcat**, le format standard est obtenu en effectuant les opérations suivantes :

  1. Tronquer les espaces blancs de début et de fin. 
  2. Analysez la formule dans une séquence de fragments des deux types suivants : 
     - Nom de champ entre crochets, c’est-à-dire. `[<field_name>]` 
     - Sous-chaîne ne contenant aucun crochet.   
      Assurez-vous qu’aucun fragment du deuxième type n’est adjacent dans la séquence. Si la formule ne peut pas être analysée de cette façon, elle est considérée comme non valide. 
  3. Effectuez le même remplacement pour les fragments du premier type que pour les champs **ftCalc** et **ftSwitch** . 
  4. Pour chaque fragment du deuxième type, échappez tous les guillemets doubles (« " ») caractères, le cas échéant, avec deux guillemets doubles consécutifs, et placez-le entre guillemets doubles. 
  5. Insérez une chaîne d’ampersand (`&`) entre chaque paire de fragments adjacents.
 
  Par exemple, à l’aide de l’Office langue de l’interface utilisateur us english, si le format d’interface utilisateur d’une formule pour un champ du type **ftConcat** est `text1 [Business Phone] "text2" [My custom field]`, où `My custom field` est le nom d’un champ défini par l’utilisateur, le format standard pour une telle formule serait `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Voir aussi

- [Exemple de flux FolderUserFields](folderuserfields-stream-sample.md)
- [Ajouter une définition pour un nouveau champ User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)

