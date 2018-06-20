---
title: Structures de flux de données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787267"
---
# <a name="stream-structures"></a>Structures de flux de données

  
  
**S’applique à**: Outlook 
  
Définitions des champs définis par l’utilisateur d’un élément de Microsoft Outlook sont stockées dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l’utilisateur et les paramètres de liaison de données pour les champs intégrés pour l’élément Outlook. Cette section fournit des informations sur la structure de l’objet stream binaire, réparti dans les structures de flux de données suivantes. 
  
> [!NOTE]
> Les noms de ces structures de flux de données (par exemple, la définition PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne sont pas techniquement partie de l’interface de programmation de l’API de messagerie (MAPI) et sont fournies ici uniquement pour la documentation à des fins des structures de flux de données réelles. Les développeurs peuvent étiqueter ces éléments de données et de structures de flux dans leurs applications leur guise. 
  
- [La définition PropertyDefinition flux Structure](propertydefinition-stream-structure.md)
    
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
    
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
    
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
    
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Voir aussi



[Les champs et les éléments outlook](outlook-items-and-fields.md)
  
[Ajoutez une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux de la définition PropertyDefinition](propertydefinition-stream-sample.md)

