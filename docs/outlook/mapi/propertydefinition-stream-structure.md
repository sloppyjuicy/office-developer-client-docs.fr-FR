---
title: Structure de flux de la définition PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b2de22eef455e59b7877524ce998e93a0a708e0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566655"
---
# <a name="propertydefinition-stream-structure"></a>Structure de flux de la définition PropertyDefinition

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une structure de flux de la définition PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un élément Microsoft Outlook et les paramètres de liaison de données pour certains champs prédéfinis. 
  
Vous pouvez manipuler par programme la structure de flux de la définition PropertyDefinition. Toutefois, vous pouvez obtenir des résultats similaires à l’aide du Concepteur de formulaires Outlook et, en particulier, la boîte de dialogue **Propriétés de** zone pour un contrôle lié aux données. 
  
Définitions de champ dans une structure de flux de la définition PropertyDefinition peuvent être une des deux formats : PropDefV1 et PropDefV2. Outlook prend en charge à la fois PropDefV1 et PropDefV2. Toutes les définitions de champ dans une structure de flux de la définition PropertyDefinition unique doivent être du même format. Pour plus d’informations sur la différence entre PropDefV1 et PropDefV2, voir [FieldDefinition flux Structure](fielddefinition-stream-structure.md).
  
Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.
  
- Version : Mot (2 octets), le format des définitions de champ dans la définition PropertyDefinition du flux de structure. Le tableau suivant présente les valeurs possibles.
    
    |**Valeur**|**Description**|
    |:-----|:-----|
    |0x0102  <br/> |Format est PropDefV1.  <br/> |
    |0x0103  <br/> |Format est PropDefV2.  <br/> |
   
- FieldDefinitionCount : DWORD (4 octets), le nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments de tableau dans l’élément de données FieldDefinitions.
    
- FieldDefinitions : Un tableau de structures de flux FieldDefinition. Le nombre de ce tableau est égal à l’élément de données FieldDefinitionCount.
    
## <a name="see-also"></a>Voir aussi

- [Champs et éléments Outlook](outlook-items-and-fields.md)
- [Ajout d’une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
- [Structures de flux](stream-structures.md)

