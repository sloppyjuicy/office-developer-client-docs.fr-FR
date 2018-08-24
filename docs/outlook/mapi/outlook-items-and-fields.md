---
title: Champs et éléments Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: caa231842c5fd51deb80144f12fdf53e51ccc980
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582874"
---
# <a name="outlook-items-and-fields"></a>Champs et éléments Outlook

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook fournit des types d’éléments qui sont spécialisés pour leurs fonctionnalités (par exemple, éléments de courrier, rendez-vous, contacts, tâches et notes). Outlook fournit des champs standard pour chaque type d’élément, souvent appelée champs intégrés. Outlook permet également aux utilisateurs de créer des champs personnalisés, communément appelé champs définis par l’utilisateur. Chaque champ est associé à un type de données et une valeur. **Devise**, **Date/heure**, **durée**, **entier**, **mots clés**et le **texte**sont des exemples de types de données. Les utilisateurs peuvent définir des champs personnalisés à l’aide du Concepteur de formulaires dans Outlook.
  
Au niveau de la programmabilité, chaque élément est représenté par un objet [IMessage](imessageimapiprop.md) . Chaque champ défini par l’utilisateur est associé à une définition de champ et une valeur. 
  
### <a name="field-definition"></a>Définition de champ

Une définition de champ inclut le nom du type de données et autres informations sur le champ. Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant. La propriété **PidLidPropertyDefinitionStream** contient un flux binaire appelé [la définition PropertyDefinition](propertydefinition-stream-structure.md) qui contient les définitions de champ. Pour plus d’informations sur les structures de flux de données pour les définitions de champ, voir [Les Structures de flux de données](stream-structures.md).
  
### <a name="field-value"></a>Valeur de champ

Chaque champ défini par l’utilisateur d’un élément a une valeur qui est stockée dans une propriété nommée correspondante. Que la propriété nommée se trouve dans le jeu de propriétés PS_PUBLIC_STRINGS et a une chaîne de caractères Unicode comme nom de propriété. Le type de données de la propriété correspond au type du champ. Si la propriété n’est pas présente dans l’objet **IMessage** , Outlook suppose une valeur par défaut de la propriété. Par exemple, pour un type de chaîne, Outlook suppose une chaîne vide si la propriété n’est pas présente. 
  
## <a name="see-also"></a>Voir aussi



[Ajout d’une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux PropertyDefinition](propertydefinition-stream-structure.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux SkipBlock](skipblock-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Structure de flux PackedAnsiString](packedansistring-stream-structure.md)
  
[Structure de flux PackedUnicodeString](packedunicodestring-stream-structure.md)

