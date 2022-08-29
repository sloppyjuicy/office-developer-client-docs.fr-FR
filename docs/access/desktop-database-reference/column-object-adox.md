---
title: Objet Column (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 90bf528e59f6a3247e4d5c8fd9ad29bed2a68060
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365571"
---
# <a name="column-object-adox"></a>Objet Column (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente une colonne dans une table, un index ou une clé.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **colonne** :

`Dim obj As New Column`

Avec les propriétés et collections d'un objet **Column**, vous pouvez :

  - Identifier la colonne à l'aide de la propriété [Name](name-property-adox.md).

  - Spécifier le type de données de la colonne à l'aide de la propriété [Type](/office/vba/access/concepts/miscellaneous/type-property-columnadox).

  - Déterminer si la colonne est à longueur fixe ou si elle peut contenir des valeurs nulles à l'aide de la propriété [Attributes](attributes-property-adox.md).

  - Spécifier la taille maximale de la colonne à l'aide de la propriété [DefinedSize](definedsize-property-adox.md).

  - Spécifier l'échelle des valeurs de données numériques à l'aide de la propriété [NumericScale](numericscale-property-adox.md).

  - Spécifier la précision maximale des valeurs de données numériques à l'aide de la propriété [Precision](precision-property-adox.md).

  - Spécifier le [catalogue](catalog-object-adox.md) auquel appartient la colonne à l'aide de la propriété [ParentCatalog](parentcatalog-property-adox.md).

  - Pour les colonnes clés, spécifier le nom de la colonne connexe dans la table connexe à l'aide de la propriété [RelatedColumn](relatedcolumn-property-adox.md).

  - Spécifier si l'ordre de tri des colonnes d'index est croissant ou décroissant à l'aide de la propriété [SortOrder](sortorder-property-adox.md).

  - Accéder aux propriétés spécifiques au fournisseur à l’aide de la collection [Properties](properties-collection-ado.md).


> [!NOTE]
> [!REMARQUE] Votre fournisseur de données peut ne pas prendre en charge toutes les propriétés des objets **Column**. Une erreur survient si vous définissez une valeur pour une propriété non prise en charge par le fournisseur. Pour les nouveaux objets **Column**, l'erreur survient lorsque l'objet est ajouté à la collection. Pour les objets existants, elle survient lors de la définition de la propriété.
> 
> Lorsque vous créez des objets **Column**, l'existence d'une valeur par défaut appropriée pour une propriété facultative ne garantit pas que votre fournisseur prend en charge la propriété. Pour plus d'informations sur les propriétés prises en charge par votre fournisseur, reportez-vous à sa documentation.

