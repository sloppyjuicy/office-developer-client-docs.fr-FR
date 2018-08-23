---
title: Structures de flux de champs de dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1ba4be04e7241a9c58138ec6b4ef72f7e0f14105
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567159"
---
# <a name="folder-fields-stream-structures"></a>Structures de flux de champs de dossier

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Propriété de [PidTagUserFields](pidtaguserfields-canonical-property.md) d’un message contient un flux binaire, FolderUserFields, qui contient les définitions de champ défini par l’utilisateur du dossier. Cette rubrique décrit les structures de flux de données pour les définitions de champ défini par l’utilisateur de dossier. 

Une structure de flux de données FolderUserFields se compose d’une structure FolderUserFieldsA ou une structure FolderUserFieldsA suivie d’une structure FolderUserFieldsW.
  
Éléments de données dans ce flux de données sont stockées immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FolderUserFieldsAnsi**: un FolderUserFieldsA flux structure.
    
- **FolderUserFieldsUnicode** (facultatif) : un FolderUserFieldsW flux structure.
    
La présence de FolderUserFieldsUnicode est détectée par la longueur totale de la FolderUserFields est supérieure à la longueur de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi est utilisé pour la compatibilité avec les ancienne, non-Unicode, les versions des clients MAPI, par conséquent, si FolderUserFieldsUnicode est présent, le contenu de FolderUserFieldsAnsi est ignorée. Pour éviter les données possibles la perte de conversion ANSI, lors de la création d’un flux de FolderUserFields toujours inclure le composant FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Structure de flux FolderUserFieldsA

Une structure de flux FolderUserFieldsA est un tableau de structures de flux FolderFieldDefinitionA qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook, sauf si le composant FolderUserFieldsW de la structure FolderUserFields.
  
Éléments de données dans ce flux de données sont stockées dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount**: DWORD (4 octets), le nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions**: un tableau de FolderFieldDefinitionA stream structures. Le nombre de ce tableau est égal à l’élément de données **FieldDefinitionCount** .
    
À moins que ce FolderUserFieldsA est remplacé par le composant FolderUserFieldsW de la structure FolderUserFields, le tableau de **FieldDefinitions** doit être « nul » en champ de Common.FieldType son dernier FolderFieldDefinitionA élément égal pour ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Structure de flux FolderUserFieldsW

Une structure de flux FolderUserFieldsW est un tableau de structures de flux FolderFieldDefinitionW qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un dossier Outlook.
  
Éléments de données dans ce flux de données sont stockées dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FieldDefinitionCount**: DWORD (4 octets), le nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments dans le tableau **FieldDefinitions** .
    
- **FieldDefinitions**: un tableau de FolderFieldDefinitionW stream structures. Le nombre de ce tableau est égal à l’élément de données **FieldDefinitionCount** .
    
Le tableau **FieldDefinitions** doit être « nul » en champ de Common.FieldType de son dernier élément FolderFieldDefinitionW égale à ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Structure de flux FolderFieldDefinitionA

Une structure de flux FolderFieldDefinitionA contient une définition d’un champ défini par l’utilisateur portant le nom de champ stocké au format ANSI.
  
Éléments de données dans ce flux de données sont stockées dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: mot (2 octets), le nombre d’éléments dans le tableau **FieldName** .
    
- **FieldName**: un tableau de CHAR. Il s’agit de la représentation sous forme de page de codes ANSI CP_ACP du nom du champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom de champ doit satisfaire les restrictions du paramètre de nom tel que spécifié dans la méthode [UserProperties.Add](http://msdn.microsoft.com/en-us/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **FieldName** ne répondant ne pas ces restrictions, mais ces cas ne sont pas couvertes par cette rubrique. 
  
- **Courantes**: stream, un FolderFieldDefinitionCommon structure.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Structure de flux FolderFieldDefinitionW

Une structure de flux FolderFieldDefinitionW contient une définition d’un champ défini par l’utilisateur portant le nom de champ stocké en Unicode.
  
Éléments de données dans ce flux de données sont stockées dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **FieldType**: FldType (4 octets), le type de ce champ.
    
- **FieldNameLength**: mot (2 octets), le nombre d’éléments dans le tableau **FieldName** .
    
- **FieldName**: un tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) du nom du champ. Le nombre de ce tableau est égal à **FieldNameLength**. Le nom de champ doit satisfaire les restrictions du paramètre de nom tel que spécifié dans la méthode [UserProperties.Add](http://msdn.microsoft.com/en-us/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **FieldName** ne répondant ne pas ces restrictions, mais celles-ci n’est pas couvertes par cette rubrique. 
  
- **Courantes**: stream, un FolderFieldDefinitionCommon structure.
    
## <a name="fldtype-enumeration"></a>Énumération FldType

Valeurs d’énumération **FldType** sont répertoriés dans le tableau suivant. 
  
|Nom|Valeur|Signification|
|:-----|:-----|:-----|
|ftNull  <br/> |0 x 0  <br/> |Ce type de champ est utilisé pour mettre fin à null un tableau des définitions de champ.  <br/> |
|ftString  <br/> |0 x 1  <br/> |Texte  <br/> |
|ftInteger  <br/> |0 x 3  <br/> |Entier  <br/> |
|ftTime  <br/> |0 x 5  <br/> |Date/Heure  <br/> |
|ftBoolean  <br/> |0 x 6  <br/> |Oui/Non  <br/> |
|ftDuration  <br/> |0 x 7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Keywords  <br/> |
|ftFloat  <br/> |0xC  <br/> |Nombre ou le pourcentage  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Monnaie  <br/> |
|ftCalc  <br/> |0 x 12  <br/> |Formule  <br/> |
|ftSwitch  <br/> |0 x 13  <br/> |Combinaison de type afficher uniquement le premier champ non vide - ignorer les suivants.  <br/> |
|ftConcat  <br/> |0 x 17  <br/> |Combinaison de type de participer à des champs et des fragments de texte à l’autre.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Structure de flux FolderFieldDefinitionCommon

Une structure de flux FolderFieldDefinitionCommon contienne les données d’une définition de champ défini par l’utilisateur qui est souvent à la fois un FolderFieldDefinitionA et un FolderFieldDefinitionW.
  
Éléments de données dans ce flux de données sont stockées dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre spécifié suivant :
  
- **PropSetGuid**: GUID (16 octets), la propriété la valeur GUID de nom de la propriété du champ dossier correspondant MAPI. Valeur de ce champ doit être égale à PS_PUBLIC_STRINGS, sauf si le type de champ est **ftNone** dans ce cas la valeur de ce champ doit être égale à la valeur GUID_NULL. 
    
   > [!NOTE]
   > Pour des raisons de compatibilité héritée, Outlook peut être en mesure de gérer certaines valeurs **PropSetGuid** ne répondant ne pas cette restriction, mais ces cas ne sont pas couvertes par cette rubrique. 
  
- **fcapm**: DWORD (4 octets), une combinaison de zéro ou plusieurs indicateurs, les valeurs qui et significations sont répertoriés dans le tableau suivant. Indicateurs avec la même valeur ont des significations VARIES selon le type de champ, c'est-à-dire FldType valeur.
    
    |Nom de l’indicateur|Valeur  |Signification|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Le champ est modifiable.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Le champ ne peut être trié.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0 x 00000004  <br/> |Le champ est être groupée.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0 x 00000100  <br/> |Le champ peut contenir plusieurs lignes de texte.  <br/> |
    |FCAPM_PERCENT  <br/> |0 x 01000000  <br/> |Ce champ de la ftFloat de type est un champ de pourcentage.  <br/> |
    |FCAPM_DATEONLY  <br/> |0 x 01000000  <br/> |Ce champ de la ftTime de type est un champ d’heure date uniquement.  <br/> |
    |FCAPM_UNITLESS  <br/> |0 x 01000000  <br/> |Pour ce champ de la ftInteger type, aucune unité n’est autorisée dans le format d’affichage ; par exemple les formats « ordinateur - 640 k... » ne sont pas autorisés.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0 x 80000000  <br/> |Le champ peut être modifié dans l’élément : il s’agit notamment des formulaires personnalisés.  <br/> |
   
- **dwString**: DWORD (4 octets). Voir la remarque suivante premier.
    
- **dwBitmap**: DWORD (4 octets). Voir la remarque suivante premier.
    
- **dwDisplay**: DWORD (4 octets). Voir la remarque suivante premier.
    
- **iFmt**: INT (4 octets). Pour les types de champs qui ont le « Format : « zone de liste déroulante dans les « Nouveau champ », « Modification du champ » et « Propriétés du champ » boîtes de dialogue de l’index de base 0 du format sélectionné dans cette zone de liste déroulante. Pour les types de champs sans cette zone de liste déroulante, il doit être 0. La valeur du champ avec le type de champ déterminent uniquement les valeurs de la **dwString**, **dwBitmap**, et **dwDisplay** champs, voir la remarque suivante premier.
    
- **wszFormulaLength**: mot (2 octets), le nombre d’éléments dans le tableau **wszFormulaLength** .
    
- **wszFormulaLength**: un tableau de WCHAR. Il s’agit de la représentation Unicode (UTF-16) de la chaîne de la formule du champ dans son format standard. Voir la remarque suivante deuxième pour la description de la norme et les formats de l’interface utilisateur de la formule d’un champ. Le nombre de ce tableau est égal à **wszFormulaLength**. La chaîne de la formule doit être une chaîne vide, sauf si le type de champ est **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Bien que les valeurs de **dwString**, **dwBitmap**et **dwDisplay** sont déterminées unique en fonction de la valeur **FldType** et la valeur **iFmt** , qui sont redondants, leurs valeurs correctes sont toujours nécessaires pour correct traitement de la définition de champ par Outlook. Il n’existe aucune description de l’algorithme qui effectue cette détermination simple. 
> 
> Par conséquent, pour trouver les valeurs de **dwString**, **dwBitmap**et **dwDisplay** correspondent à une valeur de **FldType** donné et **iFmt** , effectuez un test en créant un champ défini par l’utilisateur de ce type et ce format sélectionné dans la zone de liste déroulante **Format** , en supposant que son application, vérifiez que le flux résultant **FolderUserFields** créé par Outlook pour ce champ défini par l’utilisateur. 
  
La formule du champ dans son format de l’interface utilisateur est modifiée dans la zone de texte **formule** du **Nouveau champ** **Modification du champ**et boîtes de dialogue **Propriétés de champ** pour le champ défini par l’utilisateur. L’algorithme pour convertir une formule du format de l’interface utilisateur au format standard varie selon le type de champ comme décrit dans les éléments suivants : 
- Pour les champs de types **ftCalc** et **ftSwitch**, le format standard pour les champs intégrés, qui ne sont pas des propriétés MAPI correspondantes propriétés nommées de la nature MNID\_chaîne, est obtenu en remplaçant les fragments de nom de champ, c'est-à-dire `[<field_name>]` avec fragments `[_<field_dispid_decimal>]`. 

  Par exemple, si le format de l’interface utilisateur d’une formule pour un champ de type **formule**, qui est **ftCalc**, avec la langue de l’interface utilisateur Office en cours anglais américain, est `[Business Phone] & [My custom field]`, où `My custom field` est le nom d’un champ défini par l’utilisateur, le format standard d’une formule de ce type est `[_14856] & [My custom field]`.

- Pour les champs de la **ftConcat**de type, le format standard est obtenu en procédant comme suit :

  1. Tronquer les espaces de début et de fin. 
  2. Analyser la formule dans une séquence de fragments les deux types suivants : 
     - Un nom de champ entre crochets, autrement dit, `[<field_name>]`. 
     - Une sous-chaîne ne contenant ne pas les crochets.   
      S’assurer qu’aucune deux fragments du deuxième ne sont adjacents dans l’ordre. Si la formule ne peut pas être analysée de cette manière, il est considéré comme non valide. 
  3. Effectuer le remplacement même des fragments de premier type que pour les champs **ftCalc** et **ftSwitch** . 
  4. Pour chaque fragment du deuxième, tous les guillemet d’échappement (« « ») caractères, le cas échéant, avec deux caractères consécutifs guillemet double et mettez-le entre guillemets doubles. 
  5. Insérer une chaîne « et commercial » (`&`) entre chaque paire de fragments adjacentes.
 
  Par exemple, à l’aide de la langue de l’interface utilisateur Office anglais (États-Unis), si le format de l’interface utilisateur d’une formule pour un champ de la type **ftConcat** est `text1 [Business Phone] "text2" [My custom field]`, où `My custom field` est le nom d’un champ défini par l’utilisateur, le format standard pour une telle formule serait `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Voir aussi

- [Exemple de flux FolderUserFields](folderuserfields-stream-sample.md)
- [Ajout d’une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)

