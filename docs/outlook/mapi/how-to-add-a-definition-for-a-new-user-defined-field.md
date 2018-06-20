---
title: Ajoutez une définition pour un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783457"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Ajoutez une définition pour un nouveau champ défini par l’utilisateur
 
**S’applique à**: Outlook 
  
Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux de [la définition PropertyDefinition](propertydefinition-stream-structure.md) correspondante. Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux de la définition PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Pour ajouter une définition pour un nouveau champ défini par l’utilisateur

1. Copiez les définitions de champ existant de la structure de flux de la définition PropertyDefinition vers un nouveau tableau de définitions de champ. 
    
2. S’il y a des définitions de champ existant dans le format PropDefV1, les convertir au format PropDefV2. Pour plus d’informations sur les formats de définition de champ, voir la [Structure de flux de la définition PropertyDefinition](propertydefinition-stream-structure.md) et [FieldDefinition flux](fielddefinition-stream-structure.md).
    
3. Créer une définition du nouveau champ défini par l’utilisateur dans le format PropDefV2 et l’ajouter au tableau.
    
4. Définir l’élément de la Version de la structure de flux de la définition PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie pour cette valeur.
    
5. Incrémenter l’élément FieldDefinitionCount de 1.
    
6. Stocker en tant que la valeur de l’élément FieldDefinitions.
    
## <a name="see-also"></a>Voir aussi

- [La définition PropertyDefinition flux Structure](propertydefinition-stream-structure.md)

