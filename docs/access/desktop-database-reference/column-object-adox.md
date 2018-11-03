---
title: Column, objet (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac4416dce7d3f9fa52c4b948b1e8d3e0167c2751
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930629"
---
# <a name="column-object-adox"></a><span data-ttu-id="0825b-102">Column, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0825b-102">Column object (ADOX)</span></span>


<span data-ttu-id="0825b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0825b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0825b-104">Représente une colonne dans une table, un index ou une clé.</span><span class="sxs-lookup"><span data-stu-id="0825b-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="0825b-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="0825b-105">Remarks</span></span>

<span data-ttu-id="0825b-106">Le code suivant permet de créer une nouvelle **colonne**:</span><span class="sxs-lookup"><span data-stu-id="0825b-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="0825b-107">Avec les propriétés et collections d'un objet **Column**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0825b-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="0825b-108">Identifier la colonne à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-109">Spécifier le type de données de la colonne à l'aide de la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0825b-109">Specify the data type of the column with the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="0825b-110">Déterminer si la colonne est à longueur fixe ou si elle peut contenir des valeurs nulles à l'aide de la propriété [Attributes](attributes-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-111">Spécifier la taille maximale de la colonne à l'aide de la propriété [DefinedSize](definedsize-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-112">Spécifier l'échelle des valeurs de données numériques à l'aide de la propriété [NumericScale](numericscale-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-113">Spécifier la précision maximale des valeurs de données numériques à l'aide de la propriété [Precision](precision-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-114">Spécifier le [catalogue](catalog-object-adox.md) auquel appartient la colonne à l'aide de la propriété [ParentCatalog](parentcatalog-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-115">Pour les colonnes clés, spécifier le nom de la colonne connexe dans la table connexe à l'aide de la propriété [RelatedColumn](relatedcolumn-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-116">Spécifier si l'ordre de tri des colonnes d'index est croissant ou décroissant à l'aide de la propriété [SortOrder](sortorder-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="0825b-117">Accéder aux propriétés spécifiques au fournisseur à l'aide de la collection [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0825b-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="0825b-p101">[!REMARQUE] Votre fournisseur de données peut ne pas prendre en charge toutes les propriétés des objets **Column**. Une erreur survient si vous définissez une valeur pour une propriété non prise en charge par le fournisseur. Pour les nouveaux objets **Column**, l'erreur survient lorsque l'objet est ajouté à la collection. Pour les objets existants, elle survient lors de la définition de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0825b-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="0825b-p102">Lorsque vous créez des objets **Column**, l'existence d'une valeur par défaut appropriée pour une propriété facultative ne garantit pas que votre fournisseur prend en charge la propriété. Pour plus d'informations sur les propriétés prises en charge par votre fournisseur, reportez-vous à sa documentation.</span><span class="sxs-lookup"><span data-stu-id="0825b-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

