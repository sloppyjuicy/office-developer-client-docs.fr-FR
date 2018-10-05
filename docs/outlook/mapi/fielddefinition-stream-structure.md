---
title: Structure de flux FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383274"
---
# <a name="fielddefinition-stream-structure"></a>Structure de flux FieldDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux FieldDefinition contient la définition de champ d’un champ défini par l’utilisateur, ou un ensemble de paramètres de liaison de données pour un champ intégré.
  
Vous pouvez manipuler par programme une structure de flux FieldDefinition si la structure contient la définition de champ d’un champ défini par l’utilisateur. Vous ne devez pas essayer créer ou modifier une structure FieldDefinition si la structure contient des paramètres d’un champ intégré par programme. Vous devez utiliser le Concepteur de formulaires de Microsoft Outlook pour gérer les paramètres de ce type pour les champs intégrés.
  
> [!NOTE]
> Outlook prend en charge deux formats des définitions de champ : PropDefV1 et PropDefV2. Le format PropDefV1 des définitions de champ contient les éléments de données suivants : indicateurs, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI et ErrorANSI. Le format PropDefV2 contient les mêmes éléments et les éléments InternalType et SkipBlocks. 
>
> Outlook ne conserve pas une version Unicode pour les éléments de données FormulaANSI, ValidationRuleANSI et ValidationTextANSI dans le format de définition de champ PropDefV2. Si ces éléments contiennent des caractères non-ASCII, ces caractères peuvent être interprétées de façon incohérente en fonction de la Page de codes ANSI de l’ordinateur sur lequel Outlook est en cours d’exécution. Par conséquent, vous devez utiliser uniquement les valeurs de chaîne qui se composent de caractères ASCII pour ces éléments de données. 
  
Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.
  
- Indicateurs : DWORD (4 octets), une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
    |**Nom de l’indicateur**|**Valeur**|**Description**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La structure FieldDefinition contient une définition d’un champ défini par l’utilisateur.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher pour **une valeur est requise pour ce champ** est sélectionnée dans l’onglet **Validation** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0 x 00000004  <br/> |Un contrôle de formulaire lié à ce champ, la case à cocher pour **inclure ce champ dans Imprimer et enregistrer sous** est sélectionnée dans l’onglet **Validation** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0 x 00000008  <br/> |Pour un contrôle de formulaire lié à ce champ, la case à cocher pour **calculer cette formule automatiquement** est sélectionnée dans l’onglet **valeur** de la boîte de dialogue **Propriétés** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0 x 00000010  <br/> |Il s’agit d’un champ de type **combinaison** et elle a la possibilité de **joindre les champs et des fragments de texte entre eux** sélectionnée dans la boîte de dialogue **Champ de formule combinaison** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0 x 00000020  <br/> |Ce champ est de type **combinaison** et a l’option **Afficher uniquement le premier champ non vide, ignorer les suivants** sélectionné dans la boîte de dialogue **Champ de formule combinaison** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0 x 00000040  <br/> |Cet indicateur n’est pas utilisé par Outlook, mais il est inclus pour toutes les définitions de champ défini par l’utilisateur.  <br/> |
   
- VT : Mot (2 octets), le type de données du champ, qui est une constante de l’énumération [VARENUM](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId : DWORD (4 octets), l’identificateur de la répartition du champ. Pour un champ défini par l’utilisateur, la valeur est 0.
    
- NmidNameLength : Mot (2 octets), le nombre d’éléments dans le tableau NmidName.
    
- NmidName : Un tableau de WCHAR. Pour une définition de champ défini par l’utilisateur, il s’agit de la représentation Unicode (UTF-16) du nom du champ. Le nombre de ce tableau est égal à NmidNameLength.
    
- NameANSI : [PackedAnsiString](packedansistring-stream-structure.md) flux structure. Il s’agit de la représentation ANSI du nom du champ. 
    
- FormulaANSI : PackedAnsiString flux structure. Il s’agit d’une représentation ANSI de la formule de calcul pour le champ. Il est affiché dans la section **Valeur initiale** de l’onglet **valeur** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ValidationRuleANSI : PackedAnsiString flux structure. Il s’agit d’une représentation ANSI de formule de validation du champ. Il apparaît dans la zone de texte pour la **Formule de Validation** sur l’onglet **Validation** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ValidationTextANSI : PackedAnsiString flux structure. Il s’agit d’une représentation ANSI du texte d’échec de validation du champ. Il est affiché dans la zone de texte pour **Afficher ce message en cas d’échec de la validation de** l’onglet **Validation** de la boîte de dialogue **Propriétés** d’un contrôle de formulaire lié à ce champ. 
    
- ErrorANSI : PackedAnsiString flux structure. Outlook n’utilise pas de cet élément ; Vous devez définir cet élément à une chaîne vide.
    
- InternalType : DWORD (4 octets), le type du champ interne. Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Le type interne est une des valeurs suivantes, chacune d’elles correspond à un type dans la boîte de dialogue **Nouveau champ** pour les champs définis par l’utilisateur. 
    
    |**Nom de type interne**|**Valeur**|**Type correspondant dans la boîte de dialogue **Nouveau champ****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Pourcentage** <br/> |
    |Monnaie  <br/> |3  <br/> |**Devise** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Oui/non** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Date/Heure** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Durée** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**Combinaison**, avec l’option **Afficher uniquement le premier champ non vide, ignorer les suivants** sélectionnée dans la boîte de dialogue **Champ de formule combinaison** .  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Ce type n’est pas utilisé pour les champs définis par l’utilisateur.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Combinaison**, avec l’option **joindre les champs et des fragments de texte entre eux** sélectionnée dans la boîte de dialogue **Champ de formule combinaison** .  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Mot clé** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks : Une série d’une ou plusieurs structures de flux [SkipBlock](skipblock-stream-structure.md) . Cet élément de données est présent uniquement si le format de définition de champ est PropDefV2. Si le format de définition de champ est PropDefV2, la série doit contenir au moins une structure SkipBlock, la structure SkipBlock qui comporte l’élément de données de taille égale à 0, et la série doit commencer et se terminer par cette structure SkipBlock. 
    
   L’objectif d’une structure SkipBlock dépend de sa position relative dans la série SkipBlocks. Si la définition de champ est au format PropDefV2, et la première structure n’est pas la structure de fin (l’élément de données de taille est supérieure à 0), Outlook suppose que la première structure SkipBlock Spécifie le nom de champ en Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si le premier SkipBlock est la structure de fin, l’élément de données NameANSI est utilisé pour déterminer le nom du champ. Si cette chaîne contient des caractères non-ASCII, ces caractères peuvent être interprétés de façon incohérente en fonction de la page de codes ANSI de l’ordinateur sur lequel Outlook est en cours d’exécution. Pour éviter ces incohérences, vérifiez que vous spécifiez toujours le premier SkipBlock dans les définitions de champ que vous créez, au moins lorsque le nom de champ inclut des caractères non-ASCII. 
  
   Si une version future d’un format de définition de champ présente les éléments supplémentaires de données dans le flux FieldDefinition, ces données peuvent être stockées en tant que structures de flux SkipBlock supplémentaires de la série SkipBlocks avant la structure SkipBlock rencontrée ayant la Élément de données de taille égale à 0. Les versions antérieures d’Outlook peuvent ignorer ces structures SkipBlock supplémentaires jusqu'à la structure SkipBlock rencontrée et traiter correctement tous les blocs pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [Champs et éléments Outlook](outlook-items-and-fields.md)
- [Structures de flux](stream-structures.md)
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

