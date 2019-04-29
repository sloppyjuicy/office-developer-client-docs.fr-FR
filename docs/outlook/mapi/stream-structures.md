---
title: Structures de flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407822"
---
# <a name="stream-structures"></a>Structures de flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les définitions des champs définis par l'utilisateur d'un élément Microsoft Outlook sont stockées dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l'utilisateur et des paramètres de liaison de données pour les champs prédéfinis de l'élément Outlook. Cette section fournit des informations sur la structure du flux binaire, décomposées dans les structures de flux suivantes. 
  
> [!NOTE]
> Les noms de ces structures de flux (par exemple, PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne font pas techniquement partie de l'interface de programmation de l'API de messagerie (MAPI) et sont fournis ici uniquement pour la documentation objectifs des structures de flux réelles. Les développeurs peuvent étiqueter ces structures de flux et ces éléments de données dans leurs applications au fur et à mesure qu'ils le choisissent. 
  
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
    
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
    
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
    
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Voir aussi



[Éléments et champs Outlook](outlook-items-and-fields.md)
  
[Ajouter une définition pour un nouveau champ défini par l'utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)

