---
title: Objet Table (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6475621d711881b0187031aa037c8284e155546d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314405"
---
# <a name="table-object-adox"></a>Objet Table (ADOX)

**S’applique à** : Access 2013, Office 2013

Représente une table de base de données comprenant des colonnes, des index et des clés.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **table** :

`Dim obj As New Table`

Avec les propriétés et collections d'un objet **Table**, vous pouvez :

- Identifier la table à l'aide de la propriété [Name](name-property-adox.md).

- Déterminer le type de la table à l'aide de la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox).

- Accéder aux colonnes de base de données de la table à l'aide de la collection [Columns](columns-collection-adox.md).

- Accéder aux index de la table à l'aide de la collection [Indexes](indexes-collection-adox.md).

- Accéder aux clés de la table à l'aide de la collection [Keys](keys-collection-adox.md).

- Spécifier le [catalogue](catalog-object-adox.md) auquel appartient la table à l'aide de la propriété [ParentCatalog](parentcatalog-property-adox.md).

- Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).

- Accéder aux propriétés de table spécifiques au fournisseur à l'aide de la collection [Properties](properties-collection-ado.md).


> [!NOTE]
> [!REMARQUE] Votre fournisseur de données peut ne pas prendre en charge toutes les propriétés de l'objet **Table**. Une erreur survient si vous avez défini une valeur pour une propriété non prise en charge par le fournisseur. Pour les nouveaux objets **Table**, l'erreur survient lorsque l'objet est ajouté à la collection. Pour les objets existants, elle survient au moment de la définition de la propriété.

Lors de la création des objets **Table**, l'existence d'une valeur par défaut appropriée pour une propriété facultative ne garantit pas que votre fournisseur prend en charge la propriété. Pour plus d'informations sur les propriétés prises en charge par votre fournisseur, reportez-vous à sa documentation.

