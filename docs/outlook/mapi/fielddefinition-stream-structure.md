---
title: Structure de flux FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334894"
---
# <a name="fielddefinition-stream-structure"></a>Structure de flux FieldDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux FieldDefinition contient la définition de champ d'un champ défini par l'utilisateur ou un ensemble de paramètres de liaison de données pour un champ prédéfini.
  
Vous pouvez manipuler par programmation une structure de flux FieldDefinition si la structure contient la définition de champ d'un champ défini par l'utilisateur. Vous ne devez pas essayer de créer ou de modifier par programme une structure FieldDefinition si la structure contient des paramètres pour un champ prédéfini. Vous devez utiliser le concepteur de formulaires Microsoft Outlook pour gérer ces paramètres pour les champs intégrés.
  
> [!NOTE]
> Outlook prend en charge deux formats de définitions de champ: PropDefV1 et PropDefV2. Le format PropDefV1 des définitions de champ contient les éléments de données suivants: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI et ErrorANSI. Le format PropDefV2 contient les mêmes éléments, ainsi que les éléments InternalType et SkipBlocks. 
>
> Outlook ne gère pas de version Unicode pour les éléments de données FormulaANSI, ValidationRuleANSI et ValidationTextANSI dans le format de définition de champ PropDefV2. Si ces éléments contiennent des caractères non-ASCII, ces caractères peuvent être interprétés de manière incohérente en fonction de la page de code ANSI de l'ordinateur sur lequel Outlook est en cours d'exécution. Par conséquent, vous devez utiliser uniquement des valeurs de chaîne qui se composent entièrement de caractères ASCII pour ces éléments de données. 
  
Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.
  
- Flags: DWORD (4 octets), une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
    |**Nom de l'indicateur**|**Value**|**Description**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La structure FieldDefinition contient une définition d'un champ défini par l'utilisateur.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher d' **une valeur est obligatoire pour ce champ** est sélectionnée sous l'onglet **validation** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher **inclure ce champ pour l'impression et enregistrer sous** est sélectionnée dans l'onglet **validation** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher **calculer automatiquement cette formule** est sélectionnée dans l'onglet **valeur** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Il s'agit d'un champ de type **combinaison** dont les **champs de jonction et les fragments de texte** sont sélectionnés dans la boîte de dialogue champ de **formule de combinaison** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Ce champ est de type **combinaison** et **affiche uniquement le premier champ non vide, en ignorant** les autres options sélectionnées dans la boîte de dialogue **champ de formule de combinaison** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Cet indicateur n'est pas utilisé par Outlook, mais il est inclus pour toutes les définitions de champ définies par l'utilisateur.  <br/> |
   
- VT: WORD (2 octets), le type de données du champ, qui est une constante de l'énumération [VARENUM](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId: DWORD (4 octets), l'identificateur de répartition du champ. Pour un champ défini par l'utilisateur, la valeur est 0.
    
- NmidNameLength: WORD (2 octets), le nombre d'éléments dans le tableau NmidName.
    
- NmidName: un tableau de WCHAR. Pour une définition de champ définie par l'utilisateur, il s'agit de la représentation Unicode (UTF-16) du nom de champ. Le nombre de ce tableau est égal à NmidNameLength.
    
- NameANSI: une structure de flux de [PackedAnsiString](packedansistring-stream-structure.md) . Il s'agit de la représentation ANSI du nom de champ. 
    
- FormulaANSI: une structure de flux de PackedAnsiString. Il s'agit d'une représentation ANSI de la formule de calcul pour le champ. Elle est illustrée dans la section **valeur initiale** de l'onglet **valeur** de la boîte de dialogue **Propriétés** d'un contrôle de formulaire lié à ce champ. 
    
- ValidationRuleANSI: une structure de flux de PackedAnsiString. Il s'agit d'une représentation ANSI de la formule de validation du champ. Il est affiché dans la zone de texte de la **formule de validation** sous l'onglet **validation** de la boîte de dialogue **Propriétés** d'un contrôle de formulaire lié à ce champ. 
    
- ValidationTextANSI: une structure de flux de PackedAnsiString. Il s'agit d'une représentation ANSI du texte d'échec de validation du champ. Il est affiché dans la zone de texte pour **afficher ce message si l'** onglet **validation** échoue de la boîte de dialogue **Propriétés** d'un contrôle de formulaire lié à ce champ. 
    
- ErrorANSI: une structure de flux de PackedAnsiString. Outlook n'utilise pas cet élément; vous devez définir cet élément sur une chaîne vide.
    
- InternalType: DWORD (4 octets), le type interne du champ. Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Le type Internal est l'une des valeurs suivantes, chacune correspondant à un type dans la boîte de dialogue **nouveau champ** pour les champs définis par l'utilisateur. 
    
    |**Nom du type interne**|**Valeur**|**Type correspondant dans la boîte de dialogue **nouveau champ****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |0,1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |n°2  <br/> |**Percent** <br/> |
    |Devise  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Oui/Non** <br/> |
    |iTypeDateTime  <br/> |disque  <br/> |**Date/Heure** <br/> |
    |iTypeDuration  <br/> |6.x  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7j/7  <br/> |**Combinaison**avec l'option **afficher uniquement le premier champ non vide, en ignorant** les autres options sélectionnées dans la boîte de dialogue **champ de formule de combinaison** .  <br/> |
    |iTypeFormula  <br/> |8bits  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |4,9  <br/> |Ce type n'est pas utilisé pour les champs définis par l'utilisateur.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Ce type n'est pas utilisé pour les champs définis par l'utilisateur.  <br/> |
    |iTypeFloatResult  <br/> |a4  <br/> |Ce type n'est pas utilisé pour les champs définis par l'utilisateur.  <br/> |
    |iTypeConcat  <br/> |an  <br/> |**Combinaison**avec les **champs de jonction et tous les fragments de texte avec les autres** options sélectionnées dans la boîte de dialogue champ de formule de **combinaison** .  <br/> |
    |iTypeKeywords  <br/> |kg  <br/> |**Mot clé** <br/> |
    |iTypeInteger  <br/> |13  <br/> |**Integer** <br/> |
   
- SkipBlocks: une série d'une ou plusieurs structures de flux [SkipBlock](skipblock-stream-structure.md) . Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Si le format de définition du champ est PropDefV2, la série doit contenir au moins une structure SkipBlock, la structure SkipBlock avec l'élément de données de taille égal à 0 et la série doit commencer et se terminer par cette structure SkipBlock. 
    
   L'objectif d'une structure SkipBlock dépend de sa position relative dans la série SkipBlocks. Si la définition de champ est au format PropDefV2 et que la première structure n'est pas la structure de terminaison (l'élément de données de taille est supérieur à 0), Outlook suppose que la première structure SkipBlock spécifie le nom de champ en Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si le premier SkipBlock est la structure de terminaison, l'élément de données NameANSI est utilisé pour déterminer le nom de champ. Si cette chaîne contient des caractères non-ASCII, ceux-ci peuvent être interprétés de manière incohérente en fonction de la page de code ANSI de l'ordinateur sur lequel Outlook est en cours d'exécution. Pour éviter ce type d'incohérences, veillez à toujours spécifier le premier SkipBlock dans les définitions de champ que vous créez, au moins lorsque le nom de champ inclut des caractères non-ASCII. 
  
   Si une version ultérieure d'un format de définition de champ introduit des éléments de données supplémentaires dans le flux FieldDefinition, ces données peuvent être stockées en tant que structures de flux SkipBlock supplémentaires dans la série SkipBlocks avant la structure SkipBlock de terminaison qui a le Élément de données de taille égal à 0. Les versions antérieures d'Outlook peuvent ignorer en toute sécurité ces structures SkipBlock supplémentaires jusqu'à la fin de la SkipBlock de terminaison et traiter correctement tous les blocs qu'ils prennent en charge.
    
## <a name="see-also"></a>Voir aussi

- [Éléments et champs Outlook](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

