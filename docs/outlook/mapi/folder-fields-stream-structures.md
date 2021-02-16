---
title: Structures de flux de champs de dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336889"
---
# <a name="folder-fields-stream-structures"></a>Structures de flux de champs de dossier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La propriété [PidTagUserFields d’un](pidtaguserfields-canonical-property.md) message contient un flux binaire, FolderUserFields, qui contient les définitions de champ définies par l’utilisateur du dossier. Cette rubrique décrit les structures de flux pour les définitions de champ définies par l’utilisateur de dossier. 

Une structure de flux FolderUserFields se compose d’une structure FolderUserFieldsA ou d’une structure FolderUserFieldsA suivie d’une structure FolderUserFieldsW.
  
Les éléments de données de ce flux sont stockés immédiatement les uns après les autres dans l’ordre spécifié suivant :
  
- **FolderUserFieldsAnsi**: structure de flux FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (facultatif) : structure de flux FolderUserFieldsW.
    
La présence de FolderUserFieldsUnicode est détectée par la longueur totale de FolderUserFields supérieure à la longueur de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi est utilisé pour la compatibilité avec les versions antérieures, non Unicode, des clients MAPI. Par conséquent, si FolderUserFieldsUnicode est présent, le contenu de FolderUserFieldsAnsi est ignoré. Pour éviter toute perte de données possible dans la conversion ANSI, lors de la création d’un flux FolderUserFields, incluez toujours la partie FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA Stream Structure

Une structure de flux FolderUserFieldsA est un tableau de structures de flux FolderFieldDefinitionA qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook, sauf si le dossier FolderUserFieldsW fait partie de la structure FolderUserFields.
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount**: DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le **tableau FieldDefinitions.**
    
- **FieldDefinitions**: tableau de structures de flux FolderFieldDefinitionA. Le nombre de ce tableau est égal à **l’élément de données FieldDefinitionCount.**
    
Sauf si ce FolderUserFieldsA est annulé par la partie FolderUserFieldsW de la structure FolderUserFields, le tableau **FieldDefinitions** doit être « terminé par null » en ayant son dernier champ Common.FieldType de l’élément FolderFieldDefinitionA égal à ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Structure de flux FolderUserFieldsW

Une structure de flux FolderUserFieldsW est un tableau de structures de flux FolderFieldDefinitionW qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook.
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount**: DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le **tableau FieldDefinitions.**
    
- **FieldDefinitions**: tableau de structures de flux FolderFieldDefinitionW. Le nombre de ce tableau est égal à **l’élément de données FieldDefinitionCount.**
    
Le **tableau FieldDefinitions** doit être « terminé par null » en ayant son dernier champ Common.FieldType d’élément FolderFieldDefinitionW égal à ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA Stream Structure

Une structure de flux FolderFieldDefinitionA contient une définition d’un champ défini par l’utilisateur avec le nom de champ stocké dans ANSI.
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant :
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: WORD (2 octets), nombre d’éléments dans le tableau **FieldName.**
    
- **FieldName**: tableau de char. Il s’agit de la représentation ANSI CP_ACP page de code du nom du champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit satisfaire les restrictions sur le paramètre Name, comme spécifié dans la [méthode UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **FieldName** ne satisfaisant pas ces restrictions, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **Courant**: structure de flux FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Structure de flux FolderFieldDefinitionW

Une structure de flux FolderFieldDefinitionW contient une définition d’un champ défini par l’utilisateur avec le nom de champ stocké dans Unicode.
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant :
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: WORD (2 octets), nombre d’éléments dans le tableau **FieldName.**
    
- **FieldName :** tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) du nom du champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit satisfaire les restrictions sur le paramètre Name, comme spécifié dans la [méthode UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **FieldName** ne satisfaisant pas ces restrictions, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **Courant**: structure de flux FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>FldType, éumération

**Les valeurs d’énumération FldType** sont répertoriées dans le tableau suivant. 
  
|Nom|Valeur|Signification|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Ce type de champ est utilisé pour terminer par null un tableau de définitions de champs.  <br/> |
|ftString  <br/> |0x1  <br/> |Texte  <br/> |
|ftInteger  <br/> |0x3  <br/> |Entier  <br/> |
|ftTime  <br/> |0x5  <br/> |Date/Heure  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Oui/Non  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Mots clés  <br/> |
|ftFloat  <br/> |0xC  <br/> |Nombre ou pourcentage  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Devise  <br/> |
|ftCalc  <br/> |0x12  <br/> |Formule  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinaison de type affichant uniquement le premier champ non vide , en ignorant les champs suivants.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinaison de champs de jointage de type et de fragments de texte les uns aux autres.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Structure de flux FolderFieldDefinitionCommon

Une structure de flux FolderFieldDefinitionCommon contient les données d’une définition de champ définie par l’utilisateur commune à folderFieldDefinitionA et FolderFieldDefinitionW.
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant :
  
- **PropSetGuid**: GUID (16 octets), le GUID de jeu de propriétés du nom de propriété MAPI correspondant au champ de dossier. La valeur de ce champ doit être égale à PS_PUBLIC_STRINGS, sauf si le type de champ est **ftNone,** auquel cas la valeur de ce champ doit être égale à GUID_NULL. 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **PropSetGuid** ne satisfaisant pas cette restriction, mais ces cas ne sont pas couverts par cette rubrique. 
  
- **fcapm**: DWORD (4 octets), une combinaison de zéro ou plus indicateur les valeurs dont les valeurs et les significations sont répertoriées dans le tableau suivant. Les indicateurs avec la même valeur ont des significations qui dépendent du type du champ, autrement dit, la valeur FldType.
    
    |Nom de l’indicateur|Valeur|Signification|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Le champ est modifiable.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Le champ est triable.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Le champ est groupable.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Le champ peut contenir plusieurs lignes de texte.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Ce champ de type ftFloat est un champ de pourcentage.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Ce champ de type ftTime est un champ d’heure de date uniquement.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Pour ce champ de type ftInteger, aucune unité n’est autorisée au format d’affichage ; par exemple, des formats tels que « Ordinateur - 640 K... » ne sont pas autorisés.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Le champ peut être modifié dans l’élément : il s’agit spécifiquement des formulaires personnalisés.  <br/> |
   
- **dwString**: DWORD (4 octets). Consultez la première remarque suivante.
    
- **dwBitmap**: DWORD (4 octets). Consultez la première remarque suivante.
    
- **dwDisplay**: DWORD (4 octets). Consultez la première remarque suivante.
    
- **iFmt**: INT (4 octets). Pour les types de champs qui ont la zone de liste modifiable « Format : » dans les boîtes de dialogue « Nouveau champ », « Modifier le champ » et « Propriétés du champ », l’index de base 0 du format sélectionné dans cette zone de liste déroulante. Pour les types de champs sans cette zone de liste déroulante, ce doit être 0. La valeur du champ ainsi que le type de champ déterminent de manière unique les valeurs des champs **dwString,** **dwBitmap** et **dwDisplay,** voir la première remarque suivante.
    
- **wszFormulaLength**: WORD (2 octets), nombre d’éléments dans le tableau **wszFormulaLength.**
    
- **wszFormulaLength**: tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) de la chaîne de formule du champ dans son format standard. Consultez la deuxième remarque suivante pour obtenir la description des formats standard et d’interface utilisateur de la formule d’un champ. Le nombre de ce tableau est égal à **wszFormulaLength**. La chaîne de formule doit être une chaîne vide, sauf si le type de champ est **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Bien que les valeurs **de dwString,** **dwBitmap** et **dwDisplay** soient déterminées de manière unique en fonction de la valeur **FldType** et de la valeur **iFmt,** qui sont redondantes, leurs valeurs correctes sont toujours nécessaires pour un traitement correct de la définition de champ par Outlook. Il n’existe aucune description simple de l’algorithme qui effectue cette détermination. 
> 
> Par conséquent, pour savoir quelles valeurs **dwString,** **dwBitmap** et **dwDisplay** correspondent à une valeur **FldType** et à une valeur **iFmt** données, effectuez un test en créant un champ défini par l’utilisateur de ce type et en sélectionnant ce format dans la zone de liste déroulante **Format,** en supposant son applicabilité, examinez le flux **FolderUserFields** créé par Outlook pour ce champ défini par l’utilisateur. 
  
La formule du champ dans son format d’interface utilisateur est modifiée dans la  zone de texte Formule des boîtes de dialogue Nouveau **champ,** Modifier le champ et Propriétés du champ pour le champ défini par l’utilisateur.  L’algorithme permettant de convertir une formule du format d’interface utilisateur au format standard dépend du type de champ décrit ci-après : 
- Pour les champs de types **ftCalc** et **ftSwitch**, le format standard des champs intégrés, dont les propriétés MAPI correspondantes ne sont pas des propriétés nommées du type MNID STRING, est obtenu en remplaçant les fragments de nom de champ, c’est-à-dire par des \_ `[<field_name>]` `[_<field_dispid_decimal>]` fragments. 

  Par exemple, si le format d’interface utilisateur d’une formule pour un champ du type **Formula**, c’est-à-dire **ftCalc**, avec la langue de l’interface utilisateur Office étant anglais (États-Unis), est , où est le nom d’un champ défini par l’utilisateur, le format standard d’une telle formule serait `[Business Phone] & [My custom field]` `My custom field` `[_14856] & [My custom field]` .

- Pour les champs de type **ftConcat,** le format standard est obtenu en suivant les procédures ci-après :

  1. Tronqué les espaces de début et de fin. 
  2. Parse the formula into a sequence of fragments of the following two kinds: 
     - Nom de champ entre crochets, c’est-à-dire, `[<field_name>]` . 
     - Sous-stration ne contenant pas de crochets.   
      Assurez-vous qu’aucun des deux fragments du deuxième type n’est adjacent dans la séquence. Si la formule ne peut pas être examinée de cette façon, elle est considérée comme non valide. 
  3. Effectuez le même remplacement pour les fragments du premier type que pour les champs **ftCalc** et **ftSwitch.** 
  4. Pour chaque fragment du deuxième type, échappez à tous les guillemets doubles (« " ») s’il y en a, avec deux guillemets doubles consécutifs, et insérez-le entre guillemets doubles. 
  5. Insérez une chaîne de caractères `&` () entre chaque paire de fragments adjacents.
 
  Par exemple, à l’aide de la langue de l’interface utilisateur Office anglais (États-Unis), si le format d’interface utilisateur d’une formule pour un champ de type **ftConcat** est , où est le nom d’un champ défini par l’utilisateur, le format standard pour une telle formule serait `text1 [Business Phone] "text2" [My custom field]` `My custom field` `""text1" & [_14856] & """text2""" & [My custom field]"` . 
  
## <a name="see-also"></a>Voir aussi

- [Exemple de flux FolderUserFields](folderuserfields-stream-sample.md)
- [Ajouter une définition pour un nouveau champ User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)

