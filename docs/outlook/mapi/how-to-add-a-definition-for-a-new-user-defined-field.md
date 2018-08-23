---
title: Ajoutez une définition pour un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592716"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Ajoutez une définition pour un nouveau champ défini par l’utilisateur
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux de [la définition PropertyDefinition](propertydefinition-stream-structure.md) correspondante. Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux de la définition PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Pour ajouter une définition pour un nouveau champ défini par l’utilisateur

1. Copiez les définitions de champ existant de la structure de flux de la définition PropertyDefinition vers un nouveau tableau de définitions de champ. 
    
2. S’il y a des définitions de champ existant dans le format PropDefV1, les convertir au format PropDefV2. Pour plus d’informations sur les formats de définition de champ, voir la [Structure de flux de la définition PropertyDefinition](propertydefinition-stream-structure.md) et [FieldDefinition flux](fielddefinition-stream-structure.md).
    
3. Créer une définition du nouveau champ défini par l’utilisateur dans le format PropDefV2 et l’ajouter au tableau.
    
4. Définir l’élément de la Version de la structure de flux de la définition PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie pour cette valeur.
    
5. Incrémenter l’élément FieldDefinitionCount de 1.
    
6. Stocker en tant que la valeur de l’élément FieldDefinitions.
    
## <a name="see-also"></a>Voir aussi

- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

