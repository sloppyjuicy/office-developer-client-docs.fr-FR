---
title: Structures de flux de champs de dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336889"
---
# <a name="folder-fields-stream-structures"></a>Structures de flux de champs de dossier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La propriété [PidTagUserFields](pidtaguserfields-canonical-property.md) d'un message contient un flux binaire, FolderUserFields, qui contient les définitions de champ de dossier définies par l'utilisateur. Cette rubrique décrit les structures de flux pour les définitions de champ de dossier définies par l'utilisateur. 

Une structure de flux FolderUserFields se compose soit d'une structure FolderUserFieldsA, soit d'une structure FolderUserFieldsA suivie d'une structure FolderUserFieldsW.
  
Les éléments de données dans ce flux sont stockés immédiatement les uns les autres dans l'ordre spécifié suivant:
  
- **FolderUserFieldsAnsi**: une structure de flux de FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (facultatif): une structure de flux FolderUserFieldsW.
    
La présence de FolderUserFieldsUnicode est détectée par la longueur totale de la FolderUserFields supérieure à la longueur de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi est utilisé pour la compatibilité avec les versions antérieures, non Unicode, des clients MAPI, par conséquent si FolderUserFieldsUnicode est présent, le contenu de FolderUserFieldsAnsi est ignoré. Pour éviter toute perte de données possible dans la conversion ANSI, lors de la création d'un flux FolderUserFields, vous devez toujours inclure le composant FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Structure de flux FolderUserFieldsA

Une structure de flux FolderUserFieldsA est un tableau de structures de flux FolderFieldDefinitionA contenant les définitions de tous les champs définis par l'utilisateur dans un dossier Outlook, sauf en cas de substitution par la partie FolderUserFieldsW de la structure FolderUserFields.
  
Dans ce flux, les éléments de données sont stockés dans un ordre de primauté des octets de poids faible, immédiatement suivant l'ordre spécifié:
  
- **FieldDefinitionCount**: DWORD (4 octets), le nombre de définitions de champ dans ce flux. Il s'agit du nombre d'éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions**: tableau de structures de flux FolderFieldDefinitionA. Le nombre de ce tableau est égal à l'élément de données **FieldDefinitionCount** .
    
Sauf si cette FolderUserFieldsA est remplacée par la partie FolderUserFieldsW de la structure FolderUserFields, le tableau **FieldDefinitions** doit avoir la valeur «null-terminé» dont le dernier champ Common. FieldType de l'élément FolderFieldDefinitionA est égal vers ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Structure de flux FolderUserFieldsW

Une structure de flux FolderUserFieldsW est un tableau de structures de flux FolderFieldDefinitionW contenant des définitions pour tous les champs définis par l'utilisateur dans un dossier Outlook.
  
Dans ce flux, les éléments de données sont stockés dans un ordre de primauté des octets de poids faible, immédiatement suivant l'ordre spécifié:
  
- **FieldDefinitionCount**: DWORD (4 octets), le nombre de définitions de champ dans ce flux. Il s'agit du nombre d'éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions**: tableau de structures de flux FolderFieldDefinitionW. Le nombre de ce tableau est égal à l'élément de données **FieldDefinitionCount** .
    
Le tableau **FieldDefinitions** doit avoir la valeur «null-terminé» dont le champ Common. FieldType de l'élément FolderFieldDefinitionW a la valeur ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Structure de flux FolderFieldDefinitionA

Une structure de flux FolderFieldDefinitionA contient une définition d'un champ défini par l'utilisateur dont le nom de champ est stocké dans ANSI.
  
Dans ce flux, les éléments de données sont stockés dans un ordre de primauté des octets de poids faible, immédiatement suivant l'ordre spécifié:
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: Word (2 octets), le nombre d'éléments dans le tableau **fieldName** .
    
- **FieldName**: tableau de char. Il s'agit de la représentation de la page de codes ANSI CP_ACP du nom de champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit satisfaire aux restrictions sur le paramètre Name comme spécifié dans la méthode [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **fieldName** qui ne satisfont pas ces restrictions, mais ces cas ne sont pas abordés dans cette rubrique. 
  
- **Commun**: une structure de flux FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Structure de flux FolderFieldDefinitionW

Une structure de flux FolderFieldDefinitionW contient une définition d'un champ défini par l'utilisateur dont le nom de champ est stocké au format Unicode.
  
Dans ce flux, les éléments de données sont stockés dans un ordre de primauté des octets de poids faible, immédiatement suivant l'ordre spécifié:
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: Word (2 octets), le nombre d'éléments dans le tableau **fieldName** .
    
- **FieldName**: tableau de WCHAR. Il s'agit de la représentation Unicode (UTF-16) du nom de champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom du champ doit satisfaire aux restrictions sur le paramètre Name comme spécifié dans la méthode [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **fieldName** qui ne satisfont pas ces restrictions, mais ces cas ne sont pas abordés dans cette rubrique. 
  
- **Commun**: une structure de flux FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>FldType, énumération

Les valeurs d'énumération **FldType** sont répertoriées dans le tableau suivant. 
  
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
|ftSwitch  <br/> |0x13  <br/> |Combinaison de type affichant uniquement le premier champ non vide, en ignorant les suivants.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinaison de champs de jonction de type et de fragments de texte.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Structure de flux FolderFieldDefinitionCommon

Une structure de flux FolderFieldDefinitionCommon contient les données d'une définition de champ définie par l'utilisateur qui est commune à la fois à un FolderFieldDefinitionA et à un FolderFieldDefinitionW.
  
Dans ce flux, les éléments de données sont stockés dans un ordre de primauté des octets de poids faible, immédiatement suivant l'ordre spécifié:
  
- **PropSetGuid**: GUID (16 octets), le GUID de jeu de propriétés du nom de propriété MAPI correspondant du champ de dossier. La valeur de ce champ doit être égale à PS_PUBLIC_STRINGS, sauf si le type de champ est **ftNone** , auquel cas la valeur de ce champ doit être égale à GUID_NULL. 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **PropSetGuid** qui ne satisfont pas à cette restriction, mais ces cas ne sont pas abordés dans cette rubrique. 
  
- **fcapm**: DWORD (4 octets), une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant. Les indicateurs dont la valeur est identique ont une signification dépendante du type de champ, autrement dit, valeur FldType.
    
    |Nom de l'indicateur|Valeur|Signification|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Le champ est modifiable.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Le champ peut être trié.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Le champ peut être groupé.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Le champ peut contenir plusieurs lignes de texte.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Ce champ de type ftFloat est un champ pourcentage.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Ce champ de type ftTime est un champ date/heure uniquement.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Pour ce champ de type ftInteger, aucune unité n'est autorisée en format d'affichage; par exemple, les formats «ordinateur-640 K... non autorisés.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Le champ peut être modifié dans l'élément: il s'agit spécifiquement des formulaires personnalisés.  <br/> |
   
- **dwString**: DWORD (4 octets). Consultez la première note suivante.
    
- **dwBitmap**: DWORD (4 octets). Consultez la première note suivante.
    
- **dwDisplay**: DWORD (4 octets). Consultez la première note suivante.
    
- **iFmt**: int (4 octets). Pour les types de champs qui contiennent la zone de liste déroulante «Format:» dans les boîtes de dialogue «nouveau champ», «modifier le champ» et «propriétés du champ», l'index de base 0 du format sélectionné dans cette zone de liste déroulante. Pour les types de champs sans cette zone de liste déroulante, il doit être égal à 0. La valeur du champ ainsi que le type de champ déterminent de manière unique les valeurs des champs **dwString**, **dwBitmap**et **dwDisplay** , reportez-vous à la première note suivante.
    
- **wszFormulaLength**: Word (2 octets), le nombre d'éléments dans le tableau **wszFormulaLength** .
    
- **wszFormulaLength**: un tableau de WCHAR. Il s'agit de la représentation Unicode (UTF-16) de la formule du champ dans son format standard. Consultez la deuxième note suivante pour obtenir la description des formats standard et UI de la formule d'un champ. Le nombre de ce tableau est égal à **wszFormulaLength**. La chaîne de formule doit être une chaîne vide, sauf si le type de champ est **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Bien que les valeurs de **dwString**, **dwBitmap**et **dwDisplay** soient déterminées de manière unique en fonction de la valeur **FldType** et de la valeur **iFmt** , qui sont redondantes, leurs valeurs correctes sont toujours nécessaires pour corriger traitement de la définition de champ par Outlook. Il n'existe aucune description simple de l'algorithme qui effectue cette détermination. 
> 
> Par conséquent, pour savoir quelles valeurs **dwString**, **dwBitmap**et **DwDisplay** correspondent à une valeur **FldType** donnée et à une valeur **iFmt** , effectuez un test en créant un champ défini par l'utilisateur de ce type et avec ce format sélectionné. dans la zone de liste déroulante **format** , en supposant qu'il s'agit d'une applicabilité, inspectez le flux de **FolderUserFields** résultant créé par Outlook pour ce champ défini par l'utilisateur. 
  
La formule du champ dans son format d'interface utilisateur est modifiée dans la zone de texte **formule** des boîtes de dialogue **nouveau champ**, **champ de modification**et **Propriétés** du champ pour le champ défini par l'utilisateur. L'algorithme de conversion d'une formule du format d'interface utilisateur au format standard dépend du type de champ décrit dans les rubriques suivantes: 
- Pour les champs de types **ftCalc** et **ftSwitch**, le format standard pour les champs intégrés, qui correspondent aux propriétés MAPI qui ne sont pas des propriétés nommées de la chaîne Kind MNID\_, est obtenu en remplaçant les fragments de nom de champ, c'est-à-dire `[<field_name>]` avec des fragments `[_<field_dispid_decimal>]`. 

  Par exemple, si le format de l'interface utilisateur d'une formule pour un champ de la **formule**de type, c'est-à-dire **ftCalc**, avec la langue de l'interface utilisateur `[Business Phone] & [My custom field]`Office en `My custom field` anglais, est anglais (États-Unis), est, où est le nom d'un champ défini par l'utilisateur, le format standard de cette formule est `[_14856] & [My custom field]`.

- Pour les champs de type **ftConcat**, le format standard est obtenu en procédant comme suit:

  1. Tronque les espaces de début et de fin. 
  2. Analysez la formule dans une séquence de fragments des deux genres suivants: 
     - Nom de champ entre crochets, c'est-à-dire `[<field_name>]`. 
     - Sous-chaîne ne contenant pas de crochets.   
      Assurez-vous qu'aucun fragment du deuxième type n'est adjacent dans la séquence. Si la formule ne peut pas être analysée de cette façon, elle est considérée comme non valide. 
  3. Effectuez les mêmes remplacements pour les fragments du premier type que pour les champs **ftCalc** et **ftSwitch** . 
  4. Pour chaque fragment du deuxième type, tous les caractères guillemets doubles ("" "), le cas échéant, avec deux guillemets consécutifs, sont placés entre guillemets doubles. 
  5. Insérez une esperluette (`&`) entre chaque paire de fragments adjacents.
 
  Par exemple, à l'aide de la langue de l'interface utilisateur Office anglais (États-Unis), si le format de l' `text1 [Business Phone] "text2" [My custom field]`interface utilisateur `My custom field` d'une formule pour un champ de type **ftConcat** est, où est le nom d'un champ défini `""text1" & [_14856] & """text2""" & [My custom field]"`par l'utilisateur, le format standard de cette formule serait. 
  
## <a name="see-also"></a>Voir aussi

- [Exemple de flux FolderUserFields](folderuserfields-stream-sample.md)
- [Ajouter une définition pour un nouveau champ défini par l'utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)

