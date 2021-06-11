---
title: Structure de flux PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438588"
---
# <a name="propertydefinition-stream-structure"></a>Structure de flux PropertyDefinition

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un élément Microsoft Outlook et des paramètres de liaison de données pour certains champs intégrés. 
  
Vous pouvez manipuler par programme la structure de flux PropertyDefinition. Toutefois, vous pouvez obtenir des résultats similaires en utilisant Outlook  Forms Designer et, en particulier, la boîte de dialogue Propriétés d’un contrôle lié aux données. 
  
Les définitions de champ dans une structure de flux PropertyDefinition peuvent être l’un des deux formats : PropDefV1 et PropDefV2. Outlook prend en charge PropDefV1 et PropDefV2. Toutes les définitions de champ dans une structure de flux PropertyDefinition unique doivent être au même format. Pour plus d’informations sur la différence entre PropDefV1 et PropDefV2, voir Structure de flux [FieldDefinition.](fielddefinition-stream-structure.md)
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié ci-dessous.
  
- Version : WORD (2 octets), format des définitions de champ dans la structure de flux PropertyDefinition. Le tableau suivant montre les valeurs possibles.
    
    |**Valeur**|**Description**|
    |:-----|:-----|
    |0x0102  <br/> |Le format est PropDefV1.  <br/> |
    |0x0103  <br/> |Le format est PropDefV2.  <br/> |
   
- FieldDefinitionCount : DWORD (4 octets), nombre de définitions de champ dans ce flux. Il s’agit du nombre d’éléments de tableau dans l’élément de données FieldDefinitions.
    
- FieldDefinitions : tableau de structures de flux FieldDefinition. Le nombre de ce tableau est égal à l’élément de données FieldDefinitionCount.
    
## <a name="see-also"></a>Voir aussi

- [Outlook Éléments et champs](outlook-items-and-fields.md)
- [Ajouter une définition pour un nouveau champ User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
- [Structures de flux](stream-structures.md)

