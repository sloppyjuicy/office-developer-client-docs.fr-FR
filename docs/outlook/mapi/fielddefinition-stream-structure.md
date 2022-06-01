---
title: Structure de flux FieldDefinition
description: Cet article décrit la structure du flux FieldDefinition et l’interaction avec les éléments de données.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
ms.openlocfilehash: 94ec60bc7bf01913e2bba8cd8f10151740822445
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817927"
---
# <a name="fielddefinition-stream-structure"></a>Structure de flux FieldDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux FieldDefinition contient soit la définition de champ d’un champ défini par l’utilisateur, soit un ensemble de paramètres de liaison de données pour un champ intégré.
  
Vous pouvez manipuler par programmation une structure de flux FieldDefinition si la structure contient la définition de champ d’un champ défini par l’utilisateur. Vous ne devez pas tenter de créer ou de modifier une structure FieldDefinition par programmation si la structure contient des paramètres pour un champ intégré. Vous devez utiliser le Concepteur Microsoft Outlook Forms pour gérer ces paramètres pour les champs intégrés.
  
> [!NOTE]
> Outlook prend en charge deux formats de définitions de champ : PropDefV1 et PropDefV2. Le format PropDefV1 des définitions de champ contient les éléments de données suivants : Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI et ErrorANSI. Le format PropDefV2 contient les mêmes éléments et les éléments InternalType et SkipBlocks. 
>
> Outlook ne gère pas de version Unicode pour les éléments de données FormulaANSI, ValidationRuleANSI et ValidationTextANSI au format de définition de champ PropDefV2. Si ces éléments contiennent des caractères non ASCII, ces caractères peuvent être interprétés de manière incohérente en fonction de la page de codes ANSI de l’ordinateur sur lequel Outlook est en cours d’exécution. Par conséquent, vous devez utiliser uniquement des valeurs de chaîne composées entièrement de caractères ASCII pour ces éléments de données. 
  
Les éléments de données de ce flux sont stockés dans un ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié ci-dessous.
  
- Indicateurs : DWORD (4 octets), combinaison de zéro indicateur ou plus dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
    |**Nom de l’indicateur**|**Valeur**|**Description**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La structure FieldDefinition contient une définition d’un champ défini par l’utilisateur. |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher **A est requise pour ce champ** est sélectionnée dans l’onglet **Validation** de la boîte de dialogue **Propriétés** . |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher **Inclure ce champ pour l’impression et Enregistrer sous** est sélectionnée dans l’onglet **Validation** de la boîte de dialogue **Propriétés** . |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher **Calculer cette formule est automatiquement** sélectionnée dans l’onglet **Valeur** de la boîte de dialogue **Propriétés** . |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Il s’agit d’un champ de type **Combinaison** et il contient les **champs joints et les fragments de texte avec l’autre** option sélectionnée dans sa boîte de dialogue **Champ de formule combinée** . |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Ce champ est de type **Combinaison** et affiche **uniquement le premier champ non vide, en ignorant l’option suivante** sélectionnée dans la boîte de dialogue **Champ de formule de** combinaison. |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Cet indicateur n’est pas utilisé par Outlook, mais il est inclus pour toutes les définitions de champ définies par l’utilisateur. |
   
- VT : WORD (2 octets), type de données du champ, qui est une constante de l’énumération [VARENUM](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId : DWORD (4 octets), identificateur de répartition du champ. Pour un champ défini par l’utilisateur, la valeur est 0.
    
- NmidNameLength : WORD (2 octets), nombre d’éléments dans le tableau NmidName.
    
- NmidName : tableau de WCHAR. Pour une définition de champ définie par l’utilisateur, il s’agit de la représentation Unicode (UTF-16) du nom du champ. Le nombre de ce tableau est égal à NmidNameLength.
    
- NameANSI : structure [de flux PackedAnsiString](packedansistring-stream-structure.md) . Il s’agit de la représentation ANSI du nom du champ. 
    
- FormulaANSI : structure de flux PackedAnsiString. Il s’agit d’une représentation ANSI de la formule de calcul pour le champ. Elle s’affiche dans la section **Valeur initiale** de l’onglet **Valeur** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ValidationRuleANSI : structure de flux PackedAnsiString. Il s’agit d’une représentation ANSI de la formule de validation du champ. Elle s’affiche dans la zone de texte **de la formule de validation** sous l’onglet **Validation** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ValidationTextANSI : structure de flux PackedAnsiString. Il s’agit d’une représentation ANSI du texte d’échec de validation du champ. Il s’affiche dans la zone de texte pour **afficher ce message si la validation échoue** sous l’onglet **Validation** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ErrorANSI : structure de flux PackedAnsiString. Outlook n’utilise pas cet élément ; vous devez définir cet élément sur une chaîne vide.
    
- InternalType : DWORD (4 octets), type interne du champ. Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Le type interne est l’une des valeurs suivantes, chacune correspondant à un type dans la boîte de dialogue **Nouveau champ** pour les champs définis par l’utilisateur. 
    
    |**Nom du type interne**|**Valeur**|**Type correspondant dans la boîte de dialogue **Nouveau champ****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Pourcentage** <br/> |
    |Devise  <br/> |3  <br/> |**Devise** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Yes/No** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Date/Heure** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Combinaison**, avec **l’affichage uniquement du premier champ non vide, en ignorant l’option suivante** sélectionnée dans la boîte de dialogue **Champ de formule combinée** . |
    |iTypeFormula  <br/> |8   <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9   <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur. |
    |iTypeVariant  <br/> |10  <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur. |
    |iTypeFloatResult  <br/> |11  <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur. |
    |iTypeConcat  <br/> |12   <br/> |**Combinaison**, avec les **champs Jointure et les fragments de texte les uns avec les autres** , option sélectionnée dans la boîte de dialogue **Champ de formule combinée** . |
    |iTypeKeywords  <br/> |13  <br/> |**Mot clé** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks : série d’une ou plusieurs structures de flux [SkipBlock](skipblock-stream-structure.md) . Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Si le format de définition de champ est PropDefV2, la série doit contenir au moins une structure SkipBlock, la structure SkipBlock dont l’élément de données Size est égal à 0, et la série doit commencer et se terminer par cette structure SkipBlock. 
    
   L’objectif d’une structure SkipBlock dépend de sa position relative dans la série SkipBlocks. Si la définition de champ est au format PropDefV2 et que la première structure n’est pas la structure de fin (l’élément de données Size est supérieur à 0), Outlook suppose que la première structure SkipBlock spécifie le nom du champ dans Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si le premier SkipBlock est la structure de fin, l’élément de données NameANSI est utilisé pour déterminer le nom du champ. Si cette chaîne contient des caractères non ASCII, ces caractères peuvent être interprétés de manière incohérente en fonction de la page de codes ANSI de l’ordinateur sur lequel Outlook est en cours d’exécution. Pour éviter de telles incohérences, veillez à toujours spécifier le premier SkipBlock dans les définitions de champ que vous créez, au moins lorsque le nom du champ inclut des caractères non ASCII. 
  
   Si une version ultérieure d’un format de définition de champ introduit des éléments de données supplémentaires dans le flux FieldDefinition, ces données peuvent être stockées en tant que structures de flux SkipBlock supplémentaires dans la série SkipBlocks avant la structure SkipBlock qui met fin à la structure dont l’élément de données Size est égal à 0. Les versions antérieures de Outlook peuvent ignorer en toute sécurité ces structures SkipBlock supplémentaires jusqu’à la structure SkipBlock qui se termine et traiter correctement tous les blocs qu’elles prennent en charge.
    
## <a name="see-also"></a>Voir aussi

- [Outlook éléments et champs](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

