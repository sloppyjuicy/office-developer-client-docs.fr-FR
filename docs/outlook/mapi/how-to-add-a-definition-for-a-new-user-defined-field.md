---
title: Ajout de la définition d’un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299068"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Ajout de la définition d’un nouveau champ défini par l’utilisateur
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ajoutez un champ défini par l'utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux [PropertyDefinition](propertydefinition-stream-structure.md) correspondante. Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Pour ajouter une définition pour un nouveau champ défini par l'utilisateur

1. Copiez les définitions de champ existantes de la structure de flux PropertyDefinition vers un nouveau tableau de définitions de champs. 
    
2. Si des définitions de champ existantes sont au format PropDefV1, convertissez-les au format PropDefV2. Pour plus d'informations sur les formats de définition de champ, voir [PropertyDefinition Stream structure](propertydefinition-stream-structure.md) et [FieldDefinition Stream structure](fielddefinition-stream-structure.md).
    
3. Créez une définition du nouveau champ défini par l'utilisateur au format PropDefV2 et ajoutez-le au tableau.
    
4. Définissez l'élément version de la structure de flux PropertyDefinition en tant que 0x0103, si la valeur de l'élément version n'a pas été définie.
    
5. Incrémentez l'élément FieldDefinitionCount de 1.
    
6. Stockez le tableau en tant que valeur de l'élément FieldDefinitions.
    
## <a name="see-also"></a>Voir aussi

- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

