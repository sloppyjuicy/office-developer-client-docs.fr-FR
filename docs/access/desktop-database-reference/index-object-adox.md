---
title: Index, objet (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291774"
---
# <a name="index-object-adox"></a>Index, objet (ADOX)

**S’applique à** : Access 2013, Office 2013

Représente un index d'une table de base de données.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer un nouvel **index** :

`Dim obj As New Index`

Avec les propriétés et collections d'un objet **Index**, vous pouvez :

- Identifier l'index à l'aide de la propriété [Name](name-property-adox.md).

- Accéder aux colonnes de base de données de l'index à l'aide de la collection [Columns](columns-collection-adox.md).

- Spécifier si les clés d'index doivent être uniques à l'aide de la propriété [Unique](unique-property-adox.md).

- Spécifier si l'index est la clé primaire d'une table à l'aide de la propriété [PrimaryKey](primarykey-property-adox.md).

- Spécifier si les enregistrements dont les champs d'index contiennent des valeurs nulles ont des entrées d'index à l'aide de la propriété [IndexNulls](indexnulls-property-adox.md).

- Spécifier si l'index est organisé en clusters à l'aide de la propriété [Clustered](clustered-property-adox.md).

- Accéder aux propriétés d'index spécifiques au fournisseur à l'aide de la collection [Properties](properties-collection-ado.md).


> [!NOTE]
> [!REMARQUE] Une erreur survient lors de l'ajout d'une [colonne](column-object-adox.md) à la collection **Columns** d'un **index** si la **colonne** n'existe pas dans un objet [Table](table-object-adox.md) déjà ajouté à la collection [Tables](tables-collection-adox.md).

Votre fournisseur de données peut ne pas prendre en charge toutes les propriétés de l'objet **Index**. Une erreur survient si vous avez défini une valeur pour une propriété non prise en charge par le fournisseur. Pour les nouveaux objets **Index**, l'erreur survient lorsque l'objet est ajouté à la collection. Pour les objets existants, elle survient au moment de la définition de la propriété.

Lors de la création des objets **Index**, l'existence d'une valeur par défaut appropriée pour une propriété facultative ne garantit pas que votre fournisseur prend en charge la propriété. Pour plus d'informations sur les propriétés prises en charge par votre fournisseur, reportez-vous à sa documentation.

