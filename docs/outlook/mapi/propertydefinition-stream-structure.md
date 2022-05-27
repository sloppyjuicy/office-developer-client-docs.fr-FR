---
title: Structure de flux PropertyDefinition
description: Décrit la structure de flux PropertyDefinition, un tableau de structures de flux FieldDefinition qui peuvent être manipulées par programmation.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
ms.openlocfilehash: 05bbbe1186de994fba7e1a099f08151f5638f13f
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752721"
---
# <a name="propertydefinition-stream-structure"></a>Structure de flux PropertyDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un élément Microsoft Outlook et des paramètres de liaison de données pour certains champs intégrés. 
  
Vous pouvez manipuler la structure de flux PropertyDefinition par programmation. Toutefois, vous pouvez obtenir des résultats similaires à l’aide du concepteur Outlook Forms et, en particulier, de la boîte de dialogue **Propriétés** pour un contrôle lié aux données. 
  
Les définitions de champ dans une structure de flux PropertyDefinition peuvent être l’un des deux formats suivants : PropDefV1 et PropDefV2. Outlook prend en charge PropDefV1 et PropDefV2. Toutes les définitions de champ dans une structure de flux PropertyDefinition unique doivent avoir le même format. Pour plus d’informations sur la différence entre PropDefV1 et PropDefV2, consultez [la structure de flux FieldDefinition](fielddefinition-stream-structure.md).
  
Les éléments de données de ce flux sont stockés dans un ordre d’octet little-endian, en suivant immédiatement les uns les autres dans l’ordre spécifié ci-dessous.
  
- Version : WORD (2 octets), format des définitions de champ dans la structure de flux PropertyDefinition. Le tableau suivant montre les valeurs possibles.
    
    |**Valeur**|**Description**|
    |:-----|:-----|
    |0x0102  <br/> |Le format est PropDefV1. |
    |0x0103  <br/> |Le format est PropDefV2. |
   
- FieldDefinitionCount : DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments de tableau dans l’élément de données FieldDefinitions.
    
- FieldDefinitions : tableau de structures de flux FieldDefinition. Le nombre de ce tableau est égal à l’élément de données FieldDefinitionCount.
    
## <a name="see-also"></a>Voir aussi

- [Outlook éléments et champs](outlook-items-and-fields.md)
- [Ajouter une définition pour un nouveau champ User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
- [Structures de flux](stream-structures.md)

