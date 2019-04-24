---
title: Key, objet (référence à la base de données de bureau Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290751"
---
# <a name="key-object-adox"></a>Key, objet (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **clé** :

`Dim obj As New Key`

Avec les propriétés et collections d'un objet **Key**, vous pouvez :

- Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).

- Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).

- Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).

- Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).

- Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).

