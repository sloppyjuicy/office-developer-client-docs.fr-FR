---
title: Structures de flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581579"
---
# <a name="stream-structures"></a>Structures de flux

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définitions des champs définis par l’utilisateur d’un élément de Microsoft Outlook sont stockées dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l’utilisateur et les paramètres de liaison de données pour les champs intégrés pour l’élément Outlook. Cette section fournit des informations sur la structure de l’objet stream binaire, réparti dans les structures de flux de données suivantes. 
  
> [!NOTE]
> Les noms de ces structures de flux de données (par exemple, la définition PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne sont pas techniquement partie de l’interface de programmation de l’API de messagerie (MAPI) et sont fournies ici uniquement pour la documentation à des fins des structures de flux de données réelles. Les développeurs peuvent étiqueter ces éléments de données et de structures de flux dans leurs applications leur guise. 
  
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
    
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
    
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
    
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Voir aussi



[Champs et éléments Outlook](outlook-items-and-fields.md)
  
[Ajout d’une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)

