---
title: Outlook et champs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
ms.openlocfilehash: 6231ed5974cc3d92df9562b2e435bbb231dce914
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380703"
---
# <a name="outlook-items-and-fields"></a>Outlook et champs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Outlook types d’éléments spécialisés pour leurs fonctionnalités (par exemple, éléments de courrier, rendez-vous, contacts, tâches et notes). Outlook fournit des champs standard pour chaque type d’élément, communément appelés champs intégrés. Outlook permet également aux utilisateurs de créer des champs personnalisés, communément appelés champs définis par l’utilisateur. Chaque champ est associé à un type de données et à une valeur. Les types de données **Currency**, **Date/Time**, **Duration**, **Integer**, Keywords et Text sont des **exemples** de types **de données**. Les utilisateurs peuvent définir des champs personnalisés à l’aide du Concepteur de formulaires Outlook.
  
Au niveau de la programmabilité, chaque élément est représenté par un [objet IMessage](imessageimapiprop.md) . Chaque champ défini par l’utilisateur est associé à une définition de champ et à une valeur. 
  
### <a name="field-definition"></a>Définition de champ

Une définition de champ inclut le nom, le type de données et d’autres informations sur le champ. Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant. La **propriété PidLidPropertyDefinitionStream** contient un flux binaire appelé [PropertyDefinition](propertydefinition-stream-structure.md) qui contient les définitions de champ. Pour plus d’informations sur les structures de flux pour les définitions de champ, voir [Structures de flux](stream-structures.md).
  
### <a name="field-value"></a>Valeur de champ

Chaque champ défini par l’utilisateur d’un élément possède une valeur stockée dans une propriété nommée correspondante. Cette propriété nommée se trouve dans le jeu de PS_PUBLIC_STRINGS et possède une chaîne de caractères Unicode comme nom de propriété. Le type de données de la propriété correspond au type du champ. Si la propriété n’est pas présente dans l’objet **IMessage**, Outlook une valeur par défaut raisonnable pour la propriété. Par exemple, pour un type de chaîne, Outlook une chaîne vide si la propriété n’est pas présente. 
  
## <a name="see-also"></a>Voir aussi



[Ajouter une définition pour un nouveau User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux SkipBlock](skipblock-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString Stream Structure](packedansistring-stream-structure.md)
  
[Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

