---
title: Ajout de la définition d’un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 40da92fd14036be5b0bdd22596a120bbb4c69b2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561718"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Ajout de la définition d’un nouveau champ défini par l’utilisateur
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux [PropertyDefinition](propertydefinition-stream-structure.md) correspondante. Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Pour ajouter une définition pour un nouveau champ défini par l’utilisateur

1. Copiez les définitions de champ existantes de la structure de flux PropertyDefinition dans un nouveau tableau de définitions de champs. 
    
2. Si des définitions de champ existantes sont au format PropDefV1, convertissez-les au format PropDefV2. Pour plus d’informations sur les formats de définition de champ, voir [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) et [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Créez une définition du nouveau champ défini par l’utilisateur au format PropDefV2 et ajoutez-le au tableau.
    
4. Définissez l’élément Version de la structure de flux PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie sur cette valeur.
    
5. Incrémenter l’élément FieldDefinitionCount par 1.
    
6. Stockez le tableau en tant que valeur de l’élément FieldDefinitions.
    
## <a name="see-also"></a>Voir aussi

- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)

