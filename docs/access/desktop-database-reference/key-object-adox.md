---
title: Objet Key (référence de base de données du bureau Access - ADOX)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11bd05c4959ba1f3e1819e482ce311fc798bf0e6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929831"
---
# <a name="key-object-adox"></a>Key, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **clé**:

`Dim obj As New Key`

Avec les propriétés et collections d'un objet **Key**, vous pouvez :

- Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).

- Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).

- Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).

- Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).

- Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).

