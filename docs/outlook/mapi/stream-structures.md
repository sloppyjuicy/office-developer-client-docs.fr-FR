---
title: Structures de flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
ms.openlocfilehash: 852581d19c22cd64c18b2f49b07c50257b4d35b9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373381"
---
# <a name="stream-structures"></a>Structures de flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les définitions des champs définis par l’utilisateur d’un Outlook Microsoft sont stockées dans la [propriété PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l’utilisateur et des paramètres de liaison de données pour les champs intégrés pour l’Outlook de données. Cette section fournit des informations sur la structure du flux binaire, décomposée dans les structures de flux suivantes. 
  
> [!NOTE]
> Les noms de ces structures de flux (par exemple, PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne font techniquement pas partie de l’interface de programmation de l’API de messagerie (MAPI) et sont fournis ici uniquement à des fins de documentation des structures de flux réelles. Les développeurs peuvent étiqueter ces structures de flux et éléments de données dans leurs applications comme ils le souhaitent. 
  
- [Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
    
- [Structure de flux SkipBlock](skipblock-stream-structure.md)
    
- [Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString Stream Structure](packedansistring-stream-structure.md)
    
- [Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Voir aussi



[Outlook et champs](outlook-items-and-fields.md)
  
[Ajouter une définition pour un nouveau User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)

