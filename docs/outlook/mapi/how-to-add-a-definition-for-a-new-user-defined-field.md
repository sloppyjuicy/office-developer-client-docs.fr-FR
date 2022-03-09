---
title: Ajout de la définition d’un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
ms.openlocfilehash: b5ec432d9b3a8a4604e8fc5156181fd62f124808
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379709"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Ajout de la définition d’un nouveau champ défini par l’utilisateur
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux [PropertyDefinition](propertydefinition-stream-structure.md) correspondante. Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Pour ajouter une définition pour un nouveau champ défini par l’utilisateur

1. Copiez les définitions de champ existantes de la structure de flux PropertyDefinition dans un nouveau tableau de définitions de champs. 
    
2. Si des définitions de champ existantes sont au format PropDefV1, convertissez-les au format PropDefV2. Pour plus d’informations sur les formats de définition de champ, voir [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) et [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Créez une définition du nouveau champ défini par l’utilisateur au format PropDefV2 et ajoutez-la au tableau.
    
4. Définissez l’élément Version de la structure de flux PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie sur cette valeur.
    
5. Incrémenter l’élément FieldDefinitionCount par 1.
    
6. Stockez le tableau en tant que valeur de l’élément FieldDefinitions.
    
## <a name="see-also"></a>Voir aussi

- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

