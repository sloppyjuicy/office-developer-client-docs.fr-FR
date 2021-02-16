---
title: Éléments et champs Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409117"
---
# <a name="outlook-items-and-fields"></a>Éléments et champs Outlook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Outlook fournit des types d’éléments spécialisés pour leurs fonctionnalités (par exemple, éléments de courrier, rendez-vous, contacts, tâches et notes). Outlook fournit des champs standard pour chaque type d’élément, communément appelés champs intégrés. Outlook permet également aux utilisateurs de créer des champs personnalisés, communément appelés champs définis par l’utilisateur. Chaque champ est associé à un type de données et à une valeur. Exemples de types de données **sont Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords** et **Text**. Les utilisateurs peuvent définir des champs personnalisés à l’aide du Concepteur de formulaires dans Outlook.
  
Au niveau de la programmabilité, chaque élément est représenté par un [objet IMessage.](imessageimapiprop.md) Chaque champ défini par l’utilisateur est associé à une définition de champ et à une valeur. 
  
### <a name="field-definition"></a>Définition de champ

Une définition de champ inclut le nom, le type de données et d’autres informations sur le champ. Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant. La **propriété PidLidPropertyDefinitionStream** contient un flux binaire appelé [PropertyDefinition](propertydefinition-stream-structure.md) qui contient les définitions de champ. Pour plus d’informations sur les structures de flux pour les définitions de champ, voir [Stream Structures](stream-structures.md).
  
### <a name="field-value"></a>Valeur de champ

Chaque champ défini par l’utilisateur d’un élément possède une valeur stockée dans une propriété nommée correspondante. Cette propriété nommée se trouve dans le jeu PS_PUBLIC_STRINGS propriétés et possède une chaîne de caractères Unicode comme nom de propriété. Le type de données de la propriété correspond au type du champ. Si la propriété n’est pas présente dans l’objet **IMessage,** Outlook suppose une valeur par défaut raisonnable pour la propriété. Par exemple, pour un type de chaîne, Outlook suppose une chaîne vide si la propriété n’est pas présente. 
  
## <a name="see-also"></a>Voir aussi



[Ajouter une définition pour un nouveau champ User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux SkipBlock](skipblock-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString Stream Structure](packedansistring-stream-structure.md)
  
[Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

